# Design System Specification: Global Authority

## 1. Overview & Creative North Star

### The Creative North Star: "Precision Velocity"
This design system moves away from the static, boxy layouts typical of the logistics industry. Instead, it adopts an **Editorial Precision** aesthetic. We are not just moving parcels; we are orchestrating global trade. The UI must feel like a high-end financial broadsheet combined with a flight control center: authoritative, breathable, and hyper-efficient.

To break the "template" look, we employ **intentional asymmetry**. Hero sections should utilize large-scale typography that overlaps container boundaries, and content should follow a rhythmic, staggered flow rather than a rigid, centered grid. This creates a sense of forward motion and global reach.

---

## 2. Colors & Tonal Depth

Our palette is anchored in the authority of `primary` (#00113a) and energized by the functional "Safety" of our `tertiary` orange accents.

### The "No-Line" Rule
**Borders are a relic of the past.** In this system, 1px solid borders for sectioning are strictly prohibited. We define boundaries through **Background Color Shifts**. 
- To separate a header from a hero, transition from `surface` (#f7f9fc) to `surface-container-low` (#f2f4f7).
- To define a sidebar, use `surface-container` (#eceef1) against a `surface-bright` (#f7f9fc) main stage.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of stacked material.
- **Base Level:** `surface` (#f7f9fc)
- **Secondary Content:** `surface-container-low` (#f2f4f7)
- **Interactive Cards:** `surface-container-lowest` (#ffffff)
- **Deep Overlays:** `surface-dim` (#d8dadd)

### The "Glass & Gradient" Rule
To elevate the "Modern" requirement, floating navigation bars and modal overlays must use **Glassmorphism**. 
- **Recipe:** Apply `surface` at 80% opacity with a `24px` backdrop blur.
- **Signature Textures:** For primary CTAs and Hero backgrounds, use a subtle linear gradient from `primary` (#00113a) to `primary_container` (#002366) at a 135-degree angle. This adds a "weighted" professional polish that flat color cannot replicate.

---

## 3. Typography: The Editorial Voice

We utilize a dual-font strategy to balance corporate reliability with modern sophistication.

*   **Display & Headlines (Manrope):** Chosen for its geometric precision and modern "tech-forward" feel.
    *   `display-lg`: 3.5rem (Use for "Global" impact statements)
    *   `headline-md`: 1.75rem (Use for section titles, always left-aligned to drive the eye)
*   **Body & Labels (Inter):** The workhorse of the system. Chosen for maximum legibility in complex logistics data.
    *   `body-lg`: 1rem (Standard reading)
    *   `label-md`: 0.75rem (Uppercase, tracked out +5% for data points)

**Hierarchy Note:** Use `on_surface_variant` (#444650) for secondary body text to create a sophisticated, low-contrast hierarchy that reduces cognitive load during data-heavy tasks.

---

## 4. Elevation & Depth: Tonal Layering

We convey hierarchy through light and material, never through lines.

### The Layering Principle
Depth is achieved by stacking. A `surface-container-lowest` (#ffffff) card placed on a `surface-container` (#eceef1) background provides a "natural lift." This is our primary method of containment.

### Ambient Shadows
When an element must float (e.g., a tracking modal):
- **Shadow:** `0 20px 40px rgba(25, 28, 30, 0.06)`
- Use a tint of `on_surface` rather than pure black to keep the shadow "ambient" and integrated.

### The "Ghost Border" Fallback
If accessibility requires a border (e.g., in high-contrast modes), use a **Ghost Border**:
- `outline_variant` (#c5c6d2) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons: The Kinetic CTA
- **Primary:** Gradient of `primary` to `primary_container`. Text is `on_primary`. 
- **CTA (Action):** `tertiary_fixed_dim` (#ffb77d) background with `on_tertiary_fixed` (#2f1500) text. Use this for "Track Now" or "Book Shipment."
- **Shape:** Use `md` (0.375rem) roundedness for a corporate yet approachable feel.

### Input Fields: The Data Entry Point
- **Base:** No border. Background is `surface_container_highest` (#e0e3e6).
- **Focus State:** Bottom-only thick border (2px) in `primary` (#00113a). This mimics the "underlining" of important documents.

### Cards & Lists: The No-Divider Rule
- **Forbid dividers.** To separate list items, use `16px` of vertical white space or alternating backgrounds (`surface` and `surface_container_low`). 
- **Logistics Special:** "Tracking Chips" should use `secondary_container` (#d1e1f4) with `on_secondary_container` (#556474) for a "Slate/Steel" industrial aesthetic.

### Global Components (Context Specific)
- **The Route Map:** Utilize `inverse_surface` (#2d3133) for dark-mode map interfaces to emphasize the "Global" night-and-day operations.
- **Shipment Status Stepper:** Use `tertiary_fixed` (#ffdcc3) for the "active" path to provide high-visibility "Safety Orange" progress tracking.

---

## 6. Do’s and Don'ts

### Do:
- **Do** use aggressive white space. If a section feels finished, add 24px more padding.
- **Do** use `display-lg` typography that purposefully bleeds off the grid or overlaps image containers.
- **Do** use `tertiary` (#240f00) sparingly—only for the final conversion point or critical alerts.

### Don’t:
- **Don’t** use 1px solid #CCCCCC borders. It breaks the premium "No-Line" rule.
- **Don’t** use pure black (#000000) for text. Always use `on_surface` (#191c1e).
- **Don’t** center-align long blocks of text. Stick to the editorial left-aligned grid to maintain a "Logistics Ledger" feel.
- **Don’t** use standard Material Design shadows. They are too heavy for this high-end editorial aesthetic. Stick to the Ambient Shadow spec.