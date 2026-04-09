# Design System: High-End Legal Editorial

## 1. Overview & Creative North Star

### Creative North Star: "The Sovereign Authority"
This design system moves away from the generic, bright-blue "corporate" law firm template. Instead, it adopts the persona of a **Sovereign Authority**—an experience that feels like a private, high-stakes legal chambers after hours. It is characterized by deep tonal immersion, cinematic contrast, and an editorial layout that values silence (white space) as much as it values information.

**Breaking the Template:**
To achieve a premium feel for **Advocacia Daniel Leite**, we reject the rigid, full-width "box" mentality. We utilize:
*   **Intentional Asymmetry:** Off-center typography paired with balanced imagery to create a sense of bespoke craftsmanship.
*   **Tonal Layering:** Replacing harsh lines with shifts in surface darkness to guide the eye.
*   **The Golden Thread:** Using the `#FFD700` palette not just for buttons, but as a "light source" that pierces through the darkness to highlight critical calls to action and expertise.

---

## 2. Colors

The palette is anchored in deep obsidian and charcoal, accented by a spectrum of "legal gold" that ranges from bright highlights to rich, aged ochre.

| Token | Hex | Role |
| :--- | :--- | :--- |
| `surface` | `#131313` | The foundation. Use for the main background. |
| `primary_container` | `#FFD700` | Signature Gold. High-impact CTAs and branding accents. |
| `on_surface` | `#E5E2E1` | Primary text. A soft off-white to reduce eye strain on dark backgrounds. |
| `surface_container_low` | `#1C1B1B` | Subtle sectioning. Slightly lighter than base surface. |
| `surface_container_high` | `#2A2A2A` | Elevated card backgrounds. |
| `outline_variant` | `#4D4732` | The "Ghost Border" for ultra-subtle definition. |

### The "No-Line" Rule
Traditional 1px solid borders are strictly prohibited for sectioning or card containers. They feel "cheap" and "standard." Boundaries must be defined by:
1.  **Background Shifts:** Placing a `surface_container_low` card on a `surface` background.
2.  **Shadow Depth:** Using ambient, diffused shadows (see Section 4).

### Glass & Gradient Rule
For floating navigation bars or high-end service cards, use **Glassmorphism**:
*   `surface_container` at 60% opacity with a `24px` backdrop-blur.
*   Apply a linear gradient to the `primary_container` (Gold) transitioning from `#FFD700` to `#E9C400` to give gold accents a metallic "soul" rather than a flat yellow appearance.

---

## 3. Typography

The typographic strategy balances the historical weight of the law with the precision of modern advocacy.

### Headlines: Newsreader (Serif)
*   **Usage:** Display-lg down to Headline-sm.
*   **Personality:** Authoritative, traditional, and prestigious.
*   **Styling:** Use a slight negative letter-spacing (-0.02em) for `display-lg` to create a "tight" editorial headline feel.

### Body & UI: Inter (Sans-Serif)
*   **Usage:** Title, Body, and Labels.
*   **Personality:** Clean, objective, and highly readable.
*   **Styling:** Increase line-height to 1.6 for `body-lg` to ensure legal content feels approachable and breathable.

---

## 4. Elevation & Depth

We eschew traditional "Material" shadows in favor of a layered, physical environment.

*   **The Layering Principle:** Depth is achieved by stacking `surface-container` tiers. A `surface_container_lowest` footer creates a "grounding" effect, while `surface_container_highest` elements appear to float toward the user.
*   **Ambient Shadows:** For floating elements (like the Daniel Leite contact modal), use a shadow color of `#000000` at 40% opacity, with a `blur: 40px` and `y: 20px`. This mimics soft, natural studio lighting.
*   **The Ghost Border Fallback:** If accessibility requires a border, use `outline_variant` at **15% opacity**. This creates a "suggestion" of a container without breaking the dark-mode immersion.

---

## 5. Components

### High-Contrast Buttons
*   **Primary:** Background: `primary_container` (#FFD700); Text: `on_primary_container`. Shape: `rounded-md` (0.75rem).
*   **Interaction:** On hover, the button should scale slightly (1.02x) and increase shadow diffusion. Avoid changing the color drastically; let the gold "glow."

### Elegant Service Cards
*   **Structure:** No borders. Background: `surface_container_high`.
*   **Imagery:** Use desaturated or "tinted" imagery that blends into the `surface` color.
*   **Spacing:** Use generous padding (`xl`: 1.5rem) to allow the "Daniel Leite" expertise to feel premium.

### Form Inputs
*   **Style:** Underline-only or subtly filled containers using `surface_container_low`. 
*   **Focus State:** The label should transition to `primary_container` (Gold), and a 1px ghost-border should appear on the bottom edge.

### Forbid: Divider Lines
Horizontal and vertical dividers (HR tags) are forbidden. Use **vertical white space** (64px to 128px) or a background shift from `surface` to `surface_container_low` to mark the end of a section.

---

## 6. Do's and Don'ts

### Do
*   **DO** use Serif headings (`Newsreader`) in sentence case for a more sophisticated, legal-journal aesthetic.
*   **DO** leave "wasted" space. Premium design is defined by what you don't fill.
*   **DO** use gold accents sparingly. It is a highlighter, not a background color.

### Don't
*   **DON'T** use 100% white (`#FFFFFF`) for text. It vibrates against the deep black. Always use `on_surface` (`#E5E2E1`).
*   **DON'T** use sharp 90-degree corners. Even in a "serious" law firm, the `0.5rem` to `0.75rem` radius provides a modern, high-tech finish.
*   **DON'T** use standard "Blue" links. Every interactive element must be Gold or an underlined version of the body text.