# Design System Document: Industrial Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"Architectural Forestry."** 

We are moving away from the "generic corporate B2B" aesthetic. Instead, we are leaning into a high-end editorial feel that mirrors the precision of industrial timber processing. This system treats the digital interface as a physical construction site: robust, organized, and structurally sound, yet imbued with the warmth of natural materials. 

We break the "template" look by utilizing **Intentional Asymmetry** and **Tonal Depth**. By avoiding rigid grids in favor of overlapping elements and vast white space, we convey a sense of scale—much like a massive timber warehouse or a sprawling forest. This design system doesn't just display information; it builds a landscape for it.

## 2. Colors
Our palette is rooted in the earth but refined by industry. It uses deep, authoritative greens and warm, resinous ambers to create a premium B2B atmosphere.

### Color Strategy
*   **Primary (`#7d5800`):** Represents the "Amber Heart." Use this for key actions and brand moments.
*   **Secondary (`#795746`):** The "Raw Timber" tone. Used for supporting elements and organic depth.
*   **Surface Hierarchy:** We utilize the `surface-container` tiers to create a logical, physical stack.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit 1px solid borders for sectioning. Structural boundaries must be defined solely through background color shifts. For example, a `surface-container-low` section sitting on a `surface` background provides all the definition needed. If you feel a line is missing, use more whitespace.

### The "Glass & Gradient" Rule
To add "soul" to industrial rigidity, use subtle gradients. Transition from `primary` to `primary_container` on large CTAs. For floating navigation or over-image cards, use **Glassmorphism**: semi-transparent `surface` colors with a 12px-20px backdrop blur. This ensures the "timber" (the content) is always visible beneath the "glass" (the UI).

## 3. Typography
We utilize **Inter** for its mathematical precision and high readability in industrial contexts. The hierarchy is designed to feel like a high-end trade journal.

*   **Display (Lg/Md/Sm):** These are our "Beams." Large, bold, and authoritative. Use `display-lg` (3.5rem) for hero statements to ground the page.
*   **Headlines & Titles:** These act as "Joinery." They organize the technical specifications of the page.
*   **Body (Lg/Md):** The "Fiber." High contrast (`on_surface`) against light backgrounds ensures maximum legibility for professional B2B users.
*   **Labels:** Small, all-caps, or high-weight `label-md` tokens should be used for technical data, mimicking the stamped codes found on industrial lumber.

## 4. Elevation & Depth
In this system, depth is a result of material weight, not artificial lighting.

### The Layering Principle
Achieve hierarchy by "stacking" the surface-container tiers. 
*   **Base:** `surface`
*   **Sectioning:** `surface-container-low`
*   **Interactive Cards:** `surface-container-lowest` (to create a "lifted" paper effect) or `surface-container-high` (to create an "inset" carved effect).

### Ambient Shadows
Avoid heavy black shadows. When a "floating" effect is required (e.g., a modal), use an **Extra-Diffused Shadow**: 
*   Blur: 32px - 64px
*   Opacity: 4% - 6%
*   Color: A tinted version of `on_surface` (Dark Slate).

### The "Ghost Border" Fallback
If accessibility requires a container edge, use a "Ghost Border": the `outline_variant` token at **15% opacity**. Never use 100% opaque, high-contrast strokes.

## 5. Components

### Buttons
*   **Primary:** `primary` background with `on_primary` text. 4px-8px rounded corners. Use a subtle vertical gradient from top-left to bottom-right.
*   **Secondary:** `surface_container_high` background. No border.
*   **States:** On hover, shift the background to `primary_fixed_dim`.

### Cards
*   **Construction:** Forbid the use of divider lines. 
*   **Styling:** Use `surface-container-lowest` on top of a `surface-container-low` background. Use vertical spacing (32px+) to separate content chunks rather than lines.

### Inputs & Fields
*   **Field:** `surface_container_low` with a `ghost border` on the bottom edge only to mimic a sturdy architectural base.
*   **Labels:** Use `label-md` in `on_surface_variant` for a technical, precise look.

### Industrial Chips
*   **Style:** Sharp 4px radius. Use `secondary_container` with `on_secondary_container` text. These should look like inventory tags used in timber yards.

### Data Lists
*   Instead of dividers, use alternating "Zebra" patterns using `surface` and `surface-container-low`, or simply increased vertical padding (`body-md` with 24px padding-y).

## 6. Do's and Don'ts

### Do:
*   **Do** embrace asymmetry. Let a large image of raw timber bleed off the edge of the screen while text stays pinned to a structural grid.
*   **Do** use `primary` (Amber) sparingly as a "highlighter" for the most critical B2B conversion points.
*   **Do** use large amounts of white space (`surface`) to signify premium quality and professional organization.

### Don't:
*   **Don't** use "Drop Shadows" that look like 1990s web design. Keep them ambient and invisible.
*   **Don't** use 1px solid lines to separate content. It clutters the "site."
*   **Don't** use fully rounded (pill) buttons. This is an industrial system; we need the "structural" integrity of corners (4px-8px).
*   **Don't** use generic icons. Use high-stroke-weight, geometric industrial icons that feel like architectural blueprints.