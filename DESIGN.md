# Design System: Editorial Excellence for Isabel Molina

## 1. Overview & Creative North Star

### Creative North Star: "The Curated Perspective"
This design system moves away from the rigid, boxy constraints of standard web templates to embrace the fluid, authoritative feel of a high-end fashion or architectural magazine. It is built for a professional portfolio that treats marketing data not just as numbers, but as a narrative of success.

**The Editorial Shift:**
To achieve a "premium" feel, we reject the standard "centered container" mentality. Instead, we utilize **Intentional Asymmetry**. Large-scale typography may bleed off-center, and imagery should overlap container boundaries. We use generous white space (negative space) not as "empty room," but as a luxury element that allows Isabel’s work to breathe and command attention.

---

## 2. Colors

The palette is anchored in organic, sophisticated tones that provide a warm, "paper-like" tactile quality rather than a sterile digital feel.

- **Primary & Accents:** The `primary` (#884B3D - Muted Terracotta) is our signature. It should be used sparingly for high-impact moments: a call to action, a key metric highlight, or a pull-quote.
- **The Foundation:** The `background` (#FBF9F6 - Off-white) mimics premium heavy-stock paper. Text uses `on-surface` (#1B1C1A - Deep Charcoal) for maximum legibility with a softer edge than pure black.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to separate sections. 
Boundaries must be defined by:
1.  **Background Shifts:** Transitioning from `surface` to `surface-container-low` to signal a new thematic block.
2.  **Structural Negative Space:** Using the `16` (5.5rem) or `20` (7rem) spacing tokens to create a temporal break in the content flow.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked physical layers. 
- Place a `surface-container-lowest` card on top of a `surface-container` background to create a subtle, natural lift. 
- **The Glass Rule:** For floating navigation or modal overlays, use a semi-transparent `surface` color with a `backdrop-blur` of 12px-20px. This "Glassmorphism" ensures the editorial layout remains visible beneath the UI, maintaining a sense of depth.

---

## 3. Typography

The typography scale is the "voice" of the brand. We pair the authoritative, high-contrast **Newsreader** (Serif) with the modern, geometric clarity of **Plus Jakarta Sans** (Sans-serif).

- **Display & Headlines (Newsreader):** Use for major section breaks and "hero" statements. These should be large and unapologetic. *Styling Note:* Use tight letter-spacing (-0.02em) for `display-lg` to mimic magazine mastheads.
- **Titles & Body (Plus Jakarta Sans):** These provide the "Modern" counter-balance. Body copy should use a generous line-height (1.6) to ensure the Spanish text remains inviting and legible.
- **Labels (Plus Jakarta Sans):** Small caps or increased letter-spacing (0.05em) should be applied to `label-md` to denote metadata or "Categoría" tags.

---

## 4. Elevation & Depth

We eschew "material" shadows in favor of **Tonal Layering**.

- **The Layering Principle:** Depth is achieved by "stacking" surface tiers. A statistics card (as seen in the reference images) should not have a heavy border; it should sit as a `surface-container-lowest` (#FFFFFF) element on a `surface-container` (#EFEEEB) section.
- **Ambient Shadows:** If a floating element (like a "Contact" FAB) requires a shadow, use the `on-surface` color at 4% opacity with a blur of 40px and a Y-offset of 10px. This mimics soft, natural gallery lighting.
- **The Ghost Border:** If a boundary is strictly required for accessibility, use the `outline-variant` token at 20% opacity. This creates a "suggestion" of a line rather than a hard constraint.

---

## 5. Components

### Buttons
- **Primary:** Filled with `primary` (#884B3D), text in `on-primary` (#FFFFFF). Use `rounded-sm` (0.125rem) for a sharp, architectural look.
- **Tertiary (Editorial Link):** Underlined `title-md` text with a 2px offset. The underline should disappear on hover, replaced by a subtle background tint of `surface-container-high`.

### Cards & Data Visualization
- **Cards:** Forbid divider lines. Use `spacing-8` to separate header from content.
- **Charts:** (Inspired by the reference image) Use the `tertiary` (#1D675B) and `primary` (#884B3D) for data arcs. The "Visualizaciones" data should use `display-md` for the primary metric to ensure it feels like an editorial headline rather than a technical dashboard.

### Input Fields
- **Styling:** Use a "Minimalist Bottom-Line" approach. Only the bottom border is visible using `outline-variant`. On focus, the line transitions to `primary` with a 2px stroke. Helper text in `label-sm` should be used to guide the user in Spanish (e.g., "Por favor, introduce tu correo").

---

## 6. Do's and Don'ts

### Do
- **DO** use large, high-quality imagery that overlaps two different background color sections.
- **DO** use asymmetric margins. For example, a headline might have a `spacing-20` left margin while the body copy uses `spacing-12`.
- **DO** keep data visualizations clean. Remove all unnecessary grid lines from charts to maintain the "Magazine" aesthetic.

### Don't
- **DON'T** use 100% black (#000000). Always use the charcoal `on-surface` (#1B1C1A) to maintain the sophisticated tonal range.
- **DON'T** use `rounded-full` for buttons or containers unless it is a specific icon-only action. This system favors the structural "sharpness" of `rounded-sm` or `none`.
- **DON'T** center-align long blocks of body text. Maintain a "Left Aligned" (Ragged Right) alignment for a professional, editorial feel.