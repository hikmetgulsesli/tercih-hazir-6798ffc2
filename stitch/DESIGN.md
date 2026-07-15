---
name: Precision Status System
colors:
  surface: '#f9f9ff'
  surface-dim: '#cadbfc'
  surface-bright: '#f9f9ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f0f3ff'
  surface-container: '#e7eeff'
  surface-container-high: '#dfe8ff'
  surface-container-highest: '#d6e3ff'
  on-surface: '#091c35'
  on-surface-variant: '#434654'
  inverse-surface: '#20314b'
  inverse-on-surface: '#ecf0ff'
  outline: '#737685'
  outline-variant: '#c3c6d6'
  surface-tint: '#0c56d0'
  primary: '#003d9b'
  on-primary: '#ffffff'
  primary-container: '#0052cc'
  on-primary-container: '#c4d2ff'
  inverse-primary: '#b2c5ff'
  secondary: '#006c47'
  on-secondary: '#ffffff'
  secondary-container: '#82f9be'
  on-secondary-container: '#00734c'
  tertiary: '#5e3c00'
  on-tertiary: '#ffffff'
  tertiary-container: '#7d5200'
  on-tertiary-container: '#ffca81'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dae2ff'
  primary-fixed-dim: '#b2c5ff'
  on-primary-fixed: '#001848'
  on-primary-fixed-variant: '#0040a2'
  secondary-fixed: '#82f9be'
  secondary-fixed-dim: '#65dca4'
  on-secondary-fixed: '#002113'
  on-secondary-fixed-variant: '#005235'
  tertiary-fixed: '#ffddb3'
  tertiary-fixed-dim: '#ffb950'
  on-tertiary-fixed: '#291800'
  on-tertiary-fixed-variant: '#624000'
  background: '#f9f9ff'
  on-background: '#091c35'
  surface-variant: '#d6e3ff'
typography:
  display-lg:
    fontFamily: Hanken Grotesk
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Hanken Grotesk
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-sm:
    fontFamily: Hanken Grotesk
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  label-caps:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.05em
  status-tag:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '600'
    lineHeight: 16px
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 8px
  container-padding: 24px
  gutter: 16px
  stack-sm: 4px
  stack-md: 12px
  stack-lg: 24px
---

## Brand & Style

The design system is engineered for high-stakes operational clarity and unwavering reliability. Target users are professionals who require immediate, unambiguous data visualization to manage complex workflows. The emotional response is one of calm control and systematic order.

The aesthetic follows a **Corporate / Modern** approach with a heavy lean toward **Minimalism**. By removing unnecessary decorative elements, the design system prioritizes functional density and visual breathing room. The interface feels "airy" through generous white space, while maintaining authority through sharp execution and high-contrast information hierarchies.

## Colors

The palette is anchored in a professional "Signal Blue" for primary actions, providing a sense of institutional trust. 

- **Primary (#0052CC):** Used for primary buttons, active states, and focus indicators.
- **Success/Ready (#36B37E):** A vibrant green specifically reserved for "Ready" or "Complete" statuses to ensure instant positive reinforcement.
- **Warning (#FFAB00):** Used for "In Progress" or "Pending Review" states.
- **Neutral/Text (#42526E):** A slate gray that provides high legibility without the harshness of pure black.
- **Background (#F4F5F7):** A cool, light gray tint to differentiate the canvas from the white surface containers.

## Typography

This design system utilizes a tiered typography strategy to maximize scannability. **Hanken Grotesk** is used for headlines to provide a modern, sharp edge to the brand. **Inter** handles the heavy lifting for UI controls and body text due to its exceptional legibility at small sizes. **JetBrains Mono** is introduced sparingly for metadata and technical labels to reinforce the "tooling" and "precision" nature of the product.

For mobile devices, `display-lg` should scale down to 32px to prevent horizontal overflow while maintaining visual impact.

## Layout & Spacing

The system employs a **Fixed Grid** on desktop (12 columns, 1200px max-width) and a **Fluid Grid** on mobile (4 columns). A strict 8px base unit governs all spatial relationships.

- **Margins:** Use 24px margins on mobile to maintain white space; 40px+ on desktop to center the work area.
- **Density:** The layout favors "Roomy" padding (24px) for cards and status dashboards to prevent cognitive overload.
- **Reflow:** On mobile, side-by-side status cards stack vertically, and the primary action button pins to the bottom of the viewport for thumb-accessibility.

## Elevation & Depth

Depth is communicated through **Tonal Layers** rather than heavy shadows. The background is a cool gray, while functional areas (cards, tables) sit on pure white surfaces.

- **Layer 0 (Background):** #F4F5F7.
- **Layer 1 (Surface):** White (#FFFFFF) with a subtle 1px border (#EBECF0).
- **Interactive Elevation:** Only primary buttons and active status cards use a subtle "Ambient Shadow" (0px 4px 12px rgba(9, 30, 66, 0.08)) to indicate interactivity.
- **Outlines:** Low-contrast ghost borders are used for secondary elements to maintain a clean, flat appearance.

## Shapes

The shape language is **Soft**. 

- **Standard Elements (Buttons, Inputs):** 4px (0.25rem) radius. This creates a professional, crisp look that isn't as harsh as sharp corners but avoids the "consumer" feel of high-roundedness.
- **Status Pills:** 100px (Pill-shaped) to distinguish status indicators from clickable buttons.
- **Large Containers:** 8px (0.5rem) radius to provide a subtle structural softening for large dashboard sections.

## Components

- **Primary Action Button:** Solid Primary Blue background, white text, 4px radius. High-contrast and distinctive.
- **Status Chips:** Use a light tinted background (10% opacity of the status color) with high-contrast bold text of the same color. For "Ready", use Success Green.
- **Status Cards:** White background, 1px neutral border. When "Selected" or "Active", the border thickens to 2px Primary Blue.
- **Input Fields:** 1px neutral-gray border, turning Primary Blue on focus. Labels use `body-sm` in the Neutral-700 color.
- **Lists:** Clean rows with 1px horizontal dividers (#EBECF0). No vertical dividers to maintain a modern, airy feel.
- **Progress Indicators:** Use the secondary green for completion and the neutral gray for the remaining track to ensure the "Ready" state is the most salient visual.