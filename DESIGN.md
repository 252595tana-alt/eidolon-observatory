---
version: alpha
colors:
  background: "#e9e9df"
  background-secondary: "#ddded4"
  foreground: "#202a27"
  foreground-soft: "#394640"
  muted: "#66716a"
  forest: "#243d36"
  sea: "#17383d"
  accent-leaf: "#557b6b"
  accent-clay: "#bd7457"
  accent-sun: "#d3a477"
typography:
  japanese-body:
    fontFamily: '"Yu Gothic UI", "Hiragino Kaku Gothic ProN", "Meiryo", sans-serif'
  japanese-display:
    fontFamily: '"Yu Mincho", "Hiragino Mincho ProN", "Noto Serif JP", serif'
  utility:
    fontFamily: '"SFMono-Regular", Consolas, "Liberation Mono", monospace'
rounded:
  card: "0px"
  control: "0px"
spacing:
  page-gutter: "clamp(22px, 6vw, 88px)"
components:
  primary-link:
    border: "1px solid foreground"
    min-height: "49px"
    radius: "0px"
omitted:
  - section: elevation
    reason: "紙面と平たい展示絵を中心にし、影を装飾として使わない。"
---

## Overview

EIDOLON is a Japanese concept site introducing three imaginary landscapes through light and sound. The visual direction resembles a contemporary field notebook: mineral paper, quiet typography, hand-composed illustrations, and generous margins. The WebGL artwork is an animated tide map rather than a luminous portal. Japanese is the primary language; English appears only where it helps name the EIDOLON wordmark.

## Colors

Warm mineral paper carries the page, with a slightly darker paper tone separating the landscape index. Deep sea green and forest green anchor the WebGL artwork and final essay section. Muted leaf green and clay red appear sparingly as natural pigments. Avoid saturated violet, electric cyan, and glow effects.

## Typography

Japanese body copy uses native system sans-serif fallbacks. Display headings use Japanese Mincho system fonts for a quieter editorial voice. Monospace is reserved for small specimen numbers such as “01 / 水辺”. Use natural Japanese line wrapping and keep supporting copy readable on narrow screens.

## Layout

The header stays small and text-led. The hero pairs a Japanese title and short introduction with a rectangular animated landscape. The landscape collection uses three distinct, hand-composed illustrations rather than uniform gradient cards. A dark forest-green essay closes the page. At mobile widths, the hero stacks before the illustration and the landscape entries become a single column.

## Artwork

The hero shader draws slow topographic contours with a restrained sea, leaf, and clay palette. Pointer movement gently shifts the field; the animation pauses when the panel is off screen or the browser tab is hidden. A CSS contour field remains as a fallback when WebGL is unavailable. The three inline SVG illustrations have their own visual structures: underwater currents, branching trees, and irregular flowers.

## Components

Links are underlined on hover and remain clearly focusable by keyboard. The main action uses a square outlined treatment with a small directional arrow. The exhibit entries are editorial figures without enclosing cards or faux technical readouts. Respect the reduced-motion preference.

## Do's and Don'ts

- Let Japanese wording and the specific landscape illustrations carry the identity.
- Keep the animated tide map to one focused area of the page.
- Use small numbered field-note labels only when they add context.
- Keep the three landscape artworks visually distinct.
- Avoid invented coordinates, generic English micro-labels, orbital geometry, neon glow, and repeated glass cards.

Runtime token mapping: CSS custom properties at the top of the HTML file implement the palette, typography, and responsive page gutter. The hero fragment shader uses related colors as scene colors rather than interface accents.
