# Bridge Academy Design System

## 1. Overview & Creative North Star

### The Creative North Star: "The Academic Anchor"
Educational design often falls into the trap of being either overly rigid or childishly colorful. This design system rejects that dichotomy. "The Academic Anchor" blends the deep, authoritative weight of traditional scholarship with a modern, editorial lightness. We move beyond the "template" look by using intentional asymmetry, layered surfaces, and high-contrast typography scales that mirror the layout of a premium academic journal.

The goal is to instill immediate trust in parents while appearing approachable to students. We achieve this through **Tonal Layering** rather than hard lines, ensuring the "Bridge" between potential and achievement is reflected in a seamless, fluid digital journey.

---

## 2. Colors & Surface Philosophy

Our palette is anchored by a command-heavy Navy, supported by ethereal soft tones that provide breathing room.

### Tone & Surface Rules
*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for defining sections. Use background color shifts (e.g., a `surface-container-low` section against a `surface` background) to signify transitions.
*   **Surface Hierarchy:** Treat the UI as physical layers of fine paper. 
    *   `surface-container-lowest`: Use for primary content cards to create a "lifted" feel.
    *   `surface`: The default base.
    *   `surface-container-high`: Use for secondary utility zones.
*   **The Glass & Gradient Rule:** For hero sections and primary Call-to-Actions (CTAs), use a subtle linear gradient from `primary` (#000b29) to `primary_container` (#102147). This adds "soul" and depth that flat hex codes cannot provide.
*   **Glassmorphism:** Navigation bars and floating action elements must use semi-transparent `surface` colors with a `backdrop-blur` (12px-20px).

### Key Tokens
*   **Primary:** `#000b29` (The Anchor)
*   **Secondary:** `#495f84` (The Bridge)
*   **Background:** `#fbf9f8` (Warm Scholastic Paper)
*   **Tertiary:** `#260001` (Deep Accent for Authority)

---

## 3. Typography

The typography strategy focuses on the juxtaposition of **Public Sans** (for structural authority) and **Inter** (for high-readability Japanese/English body text).

*   **Display & Headlines (Public Sans):** Large, bold, and authoritative. These should be set with tighter letter spacing (-0.02em) to feel like premium editorial headings.
*   **Body & Labels (Inter / Sans-Serif):** High legibility is paramount. Japanese characters should be set with a generous line-height (1.7 - 1.8) to ensure academic content remains digestible and non-intimidating.
*   **Scale Influence:** Use `display-lg` (3.5rem) sparingly for high-impact brand moments. Use `headline-sm` (1.5rem) for section titles to maintain a sophisticated, balanced hierarchy.

---

## 4. Elevation & Depth

We eschew the "pasted-on" look of traditional shadows in favor of **Ambient Tonalism.**

*   **The Layering Principle:** Depth is achieved by "stacking" the surface-container tiers. A `surface-container-lowest` card placed on a `surface-container-low` background creates a soft, natural lift without the need for a drop shadow.
*   **Ambient Shadows:** If a floating element (like a mobile navigation menu) requires a shadow, it must be ultra-diffused: `blur: 40px`, `opacity: 6%`, using the `on-surface` color as the shadow base rather than pure black.
*   **The "Ghost Border":** For accessibility in input fields, use the `outline-variant` token at **15% opacity**. This provides a guide for the eye without creating a visual cage.
*   **Physicality:** Objects should feel like they have weight. Overlap elements—like a student testimonial card partially crossing into a Navy footer—to break the rigid grid and create a custom, bespoke feel.

---

## 5. Components

### Buttons
*   **Primary:** A gradient from `primary` to `primary_container`. Shape: `md` (0.75rem) roundedness. No border.
*   **Secondary:** `surface-container-lowest` background with `primary` text. Use a "Ghost Border" of 10% `outline`.
*   **Interactive State:** On hover, primary buttons should increase in saturation slightly, rather than just getting darker.

### Cards (The "Juku" Card)
*   **Style:** No borders. Background: `surface-container-lowest`. 
*   **Rounding:** `lg` (1.0rem) for a friendly, modern touch.
*   **Content:** Forbid the use of divider lines inside cards. Use vertical white space from the `1.5rem` spacing scale to separate the "Course Title" from "Pricing."

### Navigation & Footer
*   **The Bridge Menu:** High-contrast Navy (`primary`) background with `surface-container-lowest` icons. As seen in the source material, use a grid of large, clear icons for the mobile footer to ensure ease of use for parents on the go.
*   **Glass Nav:** A top navigation bar using `backdrop-blur` to allow page content to bleed through, maintaining a sense of space.

### Inputs & Chips
*   **Selection Chips:** Use `secondary_container` for the active state.
*   **Text Inputs:** Soft backgrounds (`surface_container_low`) instead of white boxes. This reduces eye strain and looks more integrated.

---

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical layouts. Let an image bleed off the side of the screen while text remains centered.
*   **Do** use "Optical Spacing." Headlines should have more space above them than below them to clearly "anchor" to their content.
*   **Do** favor `surface-tint` for subtle highlights over harsh accent colors.
*   **Do** prioritize the Japanese text readability by using the `body-lg` scale for educational descriptions.

### Don't
*   **Don't** use 100% black text. Always use `on_surface` (#1b1c1c) for a softer, more premium look.
*   **Don't** use sharp corners. Stick to the `md` and `lg` roundedness scale to keep the brand "approachable."
*   **Don't** use divider lines. If you feel you need a line, try adding `24px` of white space or a subtle background color shift instead.
*   **Don't** clutter the "Bridge Academy" logo. Give it at least `2rem` of clear space on all sides.