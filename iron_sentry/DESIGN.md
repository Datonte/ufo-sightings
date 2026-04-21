```markdown
# Design System Documentation: Tactical Precision & The Absolute Observer

## 1. Overview & Creative North Star
The design system is anchored by the Creative North Star: **"The Absolute Observer."** This is not a "hacker" aesthetic; it is a high-fidelity, sovereign intelligence environment designed for clarity, authority, and unblinking surveillance. 

To move beyond the generic "dashboard" look, this system utilizes **Functional Asymmetry** and **Information Density as Texture**. We break the traditional grid by pairing massive, high-contrast display typography with micro-scale technical data strings. The interface should feel like a piece of precision-engineered hardware—every pixel is intentional, every data point is mission-critical, and the visual weight suggests gravity and "Top Secret" clearance.

---

## 2. Colors & Tonal Architecture
The palette is rooted in deep charcoal and absolute blacks, providing a high-contrast stage for functional illumination. 

### Surface Hierarchy & The "No-Line" Rule
To achieve a premium, editorial feel, designers are prohibited from using standard 1px solid borders for general sectioning. Boundaries must be defined through **Background Color Shifts**. 
*   **Base Layer:** Use `surface` (#131313) for the primary application environment.
*   **Secondary Zones:** Use `surface_container_low` (#1c1b1b) for sidebar navigation or utility panels.
*   **Active Intel Panels:** Use `surface_container_high` (#2a2a2a) to draw the eye to critical data feeds.
*   **Nested Data:** When a container lives inside another, move one step up or down the hierarchy (e.g., a `surface_container_lowest` card sitting on a `surface_container_low` section) to create depth without visual clutter.

### The "Glass & Gradient" Rule
While the system is grounded, floating elements (like command overlays or modal alerts) must use **Glassmorphism**. Apply `surface_container` colors at 85% opacity with a `20px` backdrop blur. 
*   **Signature Glow:** Main CTAs should not be flat. Use a subtle linear gradient transitioning from `primary_fixed` (#72ff70) to `primary_container` (#00ff41) to give the "Terminal Green" a sense of phosphor-screen depth.

---

## 3. Typography
The typography strategy contrasts human-readable clarity with machine-processed technicality.

*   **Display (Space Grotesk):** Large, wide-tracking, and authoritative. Used for "CLASSIFIED" stamps and major section headers. It communicates the "High-End Editorial" nature of the system.
*   **Technical Data (Inter):** Clean, high-legibility sans-serif for body content.
*   **The Monospace Intervention:** For all numerical data, coordinates, and timestamps, use a monospace fallback (or Inter’s tabular num features). This ensures data alignment and reinforces the military-technical aesthetic.

**Hierarchy Note:** Use `display-lg` sparingly to highlight critical status codes or "TOP SECRET" designations. Use `label-sm` in all-caps with 0.1em letter spacing for "metadata labels" (e.g., LAT/LONG, USER_ID).

---

## 4. Elevation & Depth
In a surveillance environment, depth equates to data priority. 

*   **The Layering Principle:** Avoid shadows where possible. Instead, stack your `surface-container` tiers. A `surface_container_highest` element over a `surface_dim` background provides a natural, sophisticated lift.
*   **Ambient Shadows:** If a floating alert requires a shadow, it must be "Atmospheric." Use the `on_surface` color at 6% opacity with a `48px` blur and `0px` spread. This mimics the soft glow of a monitor in a dark room.
*   **The "Ghost Border" Fallback:** If containment is strictly required for accessibility, use the `outline_variant` (#3b4b37) at **15% opacity**. This creates a "suggestion" of a line that disappears into the professional darkness.

---

## 5. Components

### 0px Roundedness Scale
All components must adhere to a **0px border-radius**. This system rejects "friendly" curves in favor of the rigid, uncompromising geometry of military hardware.

### Buttons (Tactical Actuators)
*   **Primary:** Background: `primary_container` (#00ff41); Text: `on_primary` (#003907). High-visibility, used for "EXECUTE" or "CONFIRM."
*   **Secondary:** Ghost style. Background: `transparent`; Border: `outline_variant` at 20%; Text: `primary`.
*   **Tertiary (Alert):** Background: `error_container` (#93000a); Text: `on_error_container`. Reserved for "TERMINATE" or "PURGE."

### Inputs & Terminal Fields
*   **Text Inputs:** No background fill. Use a `surface_variant` bottom-border (1px) only. When focused, transition the border to `secondary_container` (Amber).
*   **Status Chips:** Rectangular. Use `secondary_fixed_dim` for "IDLE" and `primary_fixed_dim` for "TRACKING."

### Cards & Surveillance Panels
*   **No Dividers:** Prohibit the use of horizontal rules. Use a `16px` or `24px` vertical gap combined with a background shift (e.g., `surface_container_low`) to separate individual intelligence reports.
*   **Metadata Blocks:** Use `label-sm` in `on_surface_variant` to frame the corners of a card, giving it a "bracketed" look without using actual lines.

### Specialized Components: Intelligence Stamps
*   **The "Status Overlay":** A large, low-opacity (10-15%) `display-lg` text element rotated at -5 degrees, placed behind data content. Words: `TOP SECRET`, `CLASSIFIED`, `ENCRYPTED`.

---

## 6. Do’s and Don’ts

### Do:
*   **Embrace Density:** Surveillance systems are about information. Don't be afraid of data-heavy layouts; just use alignment and typography scales to manage the cognitive load.
*   **Use Functional Color:** Only use `primary_container` (Green) for success/active states, `secondary_container` (Amber) for warnings, and `alert red` for terminal errors.
*   **Align to the Grid:** Every element must feel snapped to a rigorous mathematical grid.

### Don’t:
*   **No Rounded Corners:** Never use border-radius. It breaks the "serious/technical" illusion.
*   **No Decorative Lines:** If you find yourself adding a 1px divider, ask if a `surface` color shift can do the job instead.
*   **Avoid "Sci-Fi" Tropes:** No neon glows, no spinning 3D holograms, and no "futuristic" fonts. This is a real-world, high-stakes government tool. Keep it grounded in reality.
*   **No Standard Shadows:** Avoid "drop shadows" that look like they belong on a consumer web-app. Stick to tonal layering.