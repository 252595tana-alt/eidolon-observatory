---
version: alpha
colors:
  background: "#090817"
  surface: "#100e22"
  gallery: "#e6e5ee"
  gallery-ink: "#211f37"
  gallery-muted: "#68667b"
  foreground: "#f4f1ff"
  muted: "#a5a2ba"
  accent-violet: "#b6a5ff"
  accent-ice: "#a9e7f3"
  accent-gold: "#edcfac"
typography:
  japanese:
    fontFamily: '"Hiragino Kaku Gothic ProN", "Yu Gothic", "Meiryo", sans-serif'
  display:
    fontFamily: '"Arial", "Helvetica Neue", sans-serif'
  utility:
    fontFamily: '"SFMono-Regular", Consolas, "Liberation Mono", monospace'
rounded:
  card: "0px"
  control: "0px"
spacing:
  page-gutter: "clamp(22px, 6.1vw, 94px)"
components:
  primary-link:
    border: "1px solid accent-violet at 65% opacity"
    min-height: "54px"
    radius: "0px"
omitted:
  - section: elevation
    reason: "The visual language uses emissive light and thin outlines instead of surface shadows."
---

## Overview

EIDOLON is a Japan-facing concept site for an imagined immersive digital art observatory. The audience is curious visitors arriving on desktop or mobile; the page's job is to introduce the worlds and the sensory experience. This is brand storytelling, not a booking or commerce flow. Japanese is the primary language, with English reserved for atmospheric exhibit names and small technical labels. The signature is a shader-rendered prismatic portal that responds subtly to pointer movement.

## Colors

The canvas uses ink violet as its base. Ice blue and soft violet mark the portal and key actions; muted lavender carries secondary text. The exhibition atlas shifts to moonstone gray with deep violet text, then the experience section returns to ink for a deliberate light-to-dark rhythm. Pale gold is a restrained highlight in the garden artwork and outer orbit. Color describes light and distance, not cultural motifs or status.

## Typography

Japanese copy uses native system sans-serif fallbacks so kana, kanji, and punctuation remain balanced without a remote font dependency. English exhibit names use a neutral sans-serif. Coordinates and micro-labels use monospace. Body copy starts at 16px on wide screens and may step down slightly only for compact labels and mobile supporting text; Japanese prose uses generous line height.

## Layout

The page opens with a full-viewport WebGL scene and a deliberate two-line title in the lower left. A refractive shell and two angled orbits occupy the right side on desktop and move above the copy on mobile. The exhibition atlas uses three staggered poster panels on a moonstone field, followed by a dark experience section with three explanatory feature columns. Page gutters scale with viewport width, and the exhibit cards collapse to one column on narrow screens.

## Elevation & Depth

The shader supplies depth through volumetric color, orbital geometry, and a soft vignette. Static content stays flat; thin translucent borders distinguish cards and the primary link.

## Shapes

Controls and exhibit panels are square edged. Circular geometry belongs to the celestial artwork and logo only.

## Components

The primary link uses a violet outline and an ice-blue arrow. Navigation remains text-led with a short underline on hover. Focus is always visible. All links use native anchors and preserve reduced-motion preferences.

## Do's and Don'ts

- Keep the orbital shader as the page's one dominant visual gesture; let Japanese copy remain calm and legible over it.
- Use the moonstone atlas surface to give the eye a quiet rest between the immersive hero and the final dark section.
- Use Japanese-capable system fonts before generic fallbacks and retain natural Japanese line wrapping.
- Keep exhibition names, descriptions, and imagery within the invented observatory setting.
- Do not add dense HUD chrome, unrelated neon accents, or decorative Japan stereotypes.

Runtime token mapping: the CSS custom properties at the top of `index.html` implement the palette, type, and page gutter above. WebGL colors in the fragment shader are luminous scene colors, not interface tokens.
