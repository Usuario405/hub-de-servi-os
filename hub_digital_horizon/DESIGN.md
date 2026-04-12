# Design System Document

## 1. Overview & Creative North Star: "The Digital Curator"

This design system moves beyond the standard agency template to position the brand as an authoritative, high-end digital partner. The Creative North Star is **"The Digital Curator"**—a philosophy that prizes clarity over clutter and intentionality over generic density. 

We break the "standard grid" mold by utilizing **asymmetric whitespace** and **editorial-grade typography scales**. Instead of cramming information, we curate it. The visual language is defined by expansive breathing room, city-wide authority (focused on São Paulo), and a sophisticated layering of blues that suggests depth, stability, and premium craftsmanship.

---

## 2. Colors

The palette is rooted in a spectrum of deep architectural blues and crisp, airy neutrals. We move away from "flat" design by using the Material Design tonal tiers to create a sense of environment.

### Color Tokens (Material Convention)
- **Primary:** `#005da6` (The core of our brand authority)
- **Primary Container:** `#0576cf` (Used for active states and high-impact CTAs)
- **Surface:** `#f9f9ff` (Our expansive, clean canvas)
- **Surface Container Lowest:** `#ffffff` (For elevated cards and modules)
- **On-Surface:** `#001c3b` (Deep navy for maximum readability and editorial feel)

### The "No-Line" Rule
**Explicit Instruction:** Prohibit 1px solid borders for sectioning. Boundaries must be defined solely through background color shifts. A `surface-container-low` section sitting on a `surface` background is the only way to define a change in content context. This creates a seamless, high-end "editorial" flow.

### The "Glass & Gradient" Rule
To elevate the experience, floating elements (like Navigation Bars or fixed Action Buttons) should utilize **Glassmorphism**. Apply `surface` colors at 80% opacity with a `backdrop-filter: blur(20px)`. 
- **Signature Texture:** Use a subtle linear gradient for Hero CTAs, transitioning from `primary` (#005da6) to `primary_container` (#0576cf) at a 135-degree angle. This adds "soul" to the digital interface.

---

## 3. Typography

Our typography is the backbone of the "Curator" aesthetic. We utilize **Space Grotesk** for structural impact and **Manrope** for human-centric readability.

| Level | Token | Font Family | Size | Intent |
| :--- | :--- | :--- | :--- | :--- |
| **Display** | `display-lg` | Space Grotesk | 3.5rem | High-impact hero headlines; São Paulo focus. |
| **Headline** | `headline-md` | Space Grotesk | 1.75rem | Section headers; bold and assertive. |
| **Title** | `title-lg` | Manrope | 1.375rem | Card headers and prominent sub-navigation. |
| **Body** | `body-lg` | Manrope | 1.0rem | Primary reading experience; generous line-height. |
| **Label** | `label-md` | Inter | 0.75rem | Metadata, tags, and small utility text. |

**Editorial Contrast:** Always pair a `display-lg` headline (tracking: -2%) with a `body-lg` paragraph. The contrast between the architectural weight of Space Grotesk and the neutrality of Manrope creates a professional, agency-grade rhythm.

---

## 4. Elevation & Depth

We eschew traditional drop shadows in favor of **Tonal Layering**.

- **The Layering Principle:** Place a `surface-container-lowest` (#ffffff) card on a `surface-container-low` (#f0f3ff) section. This creates a "soft lift" that feels architectural rather than "pasted on."
- **Ambient Shadows:** For floating elements, use a shadow with a 40px blur, 0px offset, and 6% opacity. Use a tint of `on-surface` (#001c3b) for the shadow color to ensure it looks like a natural occlusion of light.
- **The "Ghost Border" Fallback:** If a border is required for accessibility, use the `outline-variant` token at **15% opacity**. High-contrast, 100% opaque borders are strictly forbidden.

---

## 5. Components

### Buttons
- **Primary:** Gradient fill (`primary` to `primary_container`). Large padding (16px 32px). `xl` (1.5rem) roundedness. 
- **Secondary:** Transparent with a `primary` label. No border—use vertical whitespace to define its position.
- **State:** On hover, increase the gradient intensity; do not use a "darken" overlay.

### Cards & Service Modules
- **Rule:** Forbid the use of divider lines.
- **Style:** Use `surface-container-lowest` as the card background. Ensure the `xl` (1.5rem) corner radius is applied.
- **Content:** Emphasize city-wide coverage ("Atendimento em toda São Paulo") as a persistent label-sm element in service cards.

### Input Fields
- **Background:** `surface-container-low`.
- **Border:** Use the "Ghost Border" (15% opacity `outline-variant`).
- **Focus State:** Transition the border to 100% `primary` opacity and add a subtle 4% `primary` glow.

### Signature Component: The "São Paulo Badge"
A custom pill-shaped chip using `secondary_container` with `on_secondary_container` text, used to highlight the brand's commitment to the capital. Always located in the top-left of hero sections or footer areas.

---

## 6. Do's and Don'ts

### Do
- **DO** use asymmetric layouts. Align a headline to the left and the supporting body text to the right-center to create a modern editorial feel.
- **DO** use the Spacing Scale aggressively. If you think there is enough whitespace, add 20% more.
- **DO** use high-quality, desaturated photography with blue-toned overlays to match the `surface-variant`.

### Don't
- **DON'T** use 1px solid borders to separate sections (e.g., Header from Hero). Use a background color shift instead.
- **DON'T** use "Pure Black" (#000000). Always use `on-surface` (#001c3b) for text to maintain tonal depth.
- **DON'T** mention "8km radius" or specific neighborhood distances. Focus on the macro: "Soluções Digitais para toda São Paulo."
- **DON'T** use standard Material shadows. Stick to the extra-diffused, low-opacity Ambient Shadows defined in Section 4.