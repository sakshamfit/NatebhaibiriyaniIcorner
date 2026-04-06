# Design System Document: The Artisanal Spice Narrative

## 1. Overview & Creative North Star: "The Modern Dhaba Editorial"
This design system moves away from the cliché "fast-food" aesthetic of bright reds and yellows, pivoting instead toward a **High-End Editorial** experience. We are treating the interface like a premium lifestyle magazine dedicated to the art of the Biryani.

**Creative North Star: The Artisanal Spice Narrative.**
The goal is to evoke the sensory experience of a spice market through digital layers. We break the traditional "boxed" grid by utilizing **intentional asymmetry**, **overlapping imagery**, and **tonal depth**. The UI should feel like a curated table setting—breathable, aromatic, and tactile—balancing the raw energy of street food with the sophistication of a fine-dining establishment.

---

## 2. Colors: A Palette of Earth and Heat
Our color strategy is rooted in "Spice-Toned Sophistication." We avoid harsh blacks and stark whites in favor of organic, warm neutrals and deep, resonant pigments.

### The Color Roles
- **Primary (#8b4b00) & Primary Container (#fe9832):** Represents the deep, slow-cooked essence of Saffron and roasted spices. Use the `primary_container` for high-impact calls to action.
- **Secondary (#755700):** The "Turmeric Glow." Used for highlights, accent icons, and organic flourishes.
- **Surface & Background (#f9f6f5):** Not quite white, this "Creamy Basmati" tone provides a warm, appetizing foundation that prevents the UI from feeling sterile.
- **Inverse Surface (#0e0e0e):** Our "Charcoal/Dark Wood." Used sparingly for high-contrast moments or footer sections to ground the lighter elements.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to section content. Boundaries must be defined solely through background color shifts.
- To separate sections, transition from `surface` to `surface-container-low`.
- For internal groupings, use `surface-container-highest` backgrounds rather than a stroke.

### The "Glass & Gradient" Rule
To add "soul," use subtle linear gradients from `primary` to `primary_container` on large buttons or hero headers. For floating navigation or modal overlays, apply **Glassmorphism**: use `surface` at 80% opacity with a `24px` backdrop-blur to allow the vibrant food photography to bleed through the UI.

---

## 3. Typography: Bilingual Harmony
We pair **Be Vietnam Pro** (for its geometric modernism) with **Plus Jakarta Sans** (for its high legibility). This system is designed to treat Devanagari and Latin scripts with equal weight and beauty.

- **Display (Be Vietnam Pro):** Use `display-lg` (3.5rem) for hero headlines. Ensure tight letter-spacing (-0.02em) to create an editorial "poster" feel.
- **Headline (Be Vietnam Pro):** Use `headline-lg` (2rem) for section titles. This font’s clean terminals mirror the modern, premium side of the brand.
- **Body (Plus Jakarta Sans):** Use `body-lg` (1rem) for descriptions. Its open counters ensure readability even when layered over subtle "spice dust" textures.
- **Label (Plus Jakarta Sans):** Use `label-md` (0.75rem) in All-Caps with 0.05em tracking for category tags, mimicking the look of traditional spice jar labels.

---

## 4. Elevation & Depth: Tonal Layering
We reject the standard "shadow-on-white" approach. Instead, we use **Tonal Layering** to create a 3D-like physical presence.

- **The Layering Principle:** Depth is achieved by stacking containers.
    1. Base: `surface`
    2. Section: `surface-container-low`
    3. Card/Element: `surface-container-lowest` (This creates a "lifted" effect without a shadow).
- **Ambient Shadows:** When a true float is needed (e.g., a floating Biryani bowl image), use a shadow tinted with `on-surface` at 6% opacity, with a blur radius of `40px` and a `12px` Y-offset. It should feel like an ambient glow, not a drop shadow.
- **The "Ghost Border" Fallback:** If a container sits on an identical background, use the `outline_variant` at 15% opacity. Never use 100% opaque lines.
- **Signature Texture Overlay:** Apply a subtle noise or "spice dust" texture (at 3% opacity) over `surface-container` tiers to give the digital surface a tactile, paper-like quality.

---

## 5. Components

### Buttons: The "Saffron" CTAs
- **Primary:** Background `primary_container`, Text `on_primary_container`. Shape: `xl` (1.5rem) roundedness for a friendly, modern feel.
- **Secondary:** Background `surface_container_highest`, Text `primary`. No border.
- **Tertiary:** Text `primary` with a subtle underline in `primary_fixed_dim`.

### Cards: The "Ingredient" Layout
- **Style:** No borders. Use `surface_container_low` as the card background.
- **Imagery:** Food images should "break" the card container. For example, a Biryani pot should overlap the top edge of the card by 20px, utilizing a soft ambient shadow to create a 3D pop.

### Inputs: The "Minimalist Pantry"
- **Style:** Use a "Filled" style with `surface_container_highest`. 
- **Indicator:** Use a 2px bottom bar in `primary` only during the `focus` state.
- **Labels:** Always use `label-md` in `on_surface_variant`.

### Chips: The "Spice Tags"
- **Style:** `surface-container-lowest` with a `sm` (0.25rem) radius. 
- **Selection:** Transition to `primary_container` when active. Avoid heavy shadows; use a 10% `primary` glow.

### Lists: Vertical Breathing Room
- **Rule:** Forbid divider lines. Separate list items using the **Spacing Scale** (minimum 24px) or by alternating background tones between `surface` and `surface-container-lowest`.

---

## 6. Do’s and Don’ts

### Do:
- **Do** overlap text and imagery. A headline should slightly "tuck" behind a high-quality cutout of a spice sprig or a bowl.
- **Do** use intentional asymmetry. Align your headlines to the left but float your "Order Now" button to a slightly off-center right to create visual interest.
- **Do** use the `secondary_fixed` (Turmeric) for micro-interactions like star ratings or "Chef's Recommended" badges.

### Don't:
- **Don’t** use pure black (#000000) for text. Use `on_surface` (#2f2f2e) to maintain the "warm" organic feel.
- **Don’t** use standard "out-of-the-box" Material ripples. Use a soft scale-up animation (1.02x) for hover states to mimic physical engagement.
- **Don’t** pack elements tightly. This is a premium experience; white space (or "Spice Space") is your most valuable asset to convey luxury.

---
*End of Document*