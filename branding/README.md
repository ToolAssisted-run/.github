# ToolAssisted.run Brand

The mark is a **TAStudio input timeline**: frames flowing downward through a piano
roll of pressed inputs, with the playhead in Signal Green — the way every TAS is
actually made, one frame at a time.

## Files

| File | Use |
|---|---|
| `logo.svg` | Canonical lockup, text as outlines (no fonts needed). Ink uses `currentColor` (default `#0F172A`); recolor ink via CSS `color`. |
| `logo-light.svg` / `logo-dark.svg` | Fixed-ink variants for contexts without CSS control (light = ink `#0F172A`, dark = ink `#F1F5F9`). |
| `icon.svg` (+ `-light`/`-dark`) | Standalone timeline mark, square, transparent. |
| `avatar-dark.svg` / `avatar-light.svg` | Full-bleed square: mark + `toolAssisted.run` URL underneath (text as outlines), maximized edge-to-edge. Dark = `#0B1220` plate for dark contexts; light = white plate for white backgrounds. Note: circle-crop platforms (Twitter/Discord) clip the first/last ~2 characters of the URL — accepted trade-off for size. |
| `icon-labeled.svg` (+ `-light`/`-dark`) | Same mark + URL, transparent, ink via `currentColor` — for square placements on arbitrary surfaces. |
| `png/logo-{light,dark}.png` | Ready-to-use lockup renders. |
| `png/icon-{512,256,64,32,16}.png` (+ `-dark`) | Favicons / app icons (transparent, bare mark — no URL). Default = light-surface ink; `-dark` = light ink for dark surfaces. |
| `png/icon-labeled-{512,256}-{light,dark}.png` | Labeled icon renders. |
| `png/avatar-{512,256,128,64}-{dark,light}.png` | Profile pictures (with URL), both plate colors. |
| `concepts/` | The exploration that led here (4 concepts, color studies, piano-roll variation sheet). |

## Palette

| Token | Hex | Role |
|---|---|---|
| Signal Green | `#22C55E` | Accent: the playhead, `.run`, links/actions. The color of a passing sync check. |
| Ink | `#0F172A` | Text/mark on light backgrounds. |
| Ink (dark mode) | `#F1F5F9` | Text/mark on dark backgrounds. |
| Plate | `#0B1220` | Dark background / avatar plate. |
| Muted | `#64748B` / `#94A3B8` | Secondary text (light / dark mode). |

Unpressed cells are Ink at 18% opacity; pressed cells are full Ink.

Note: Signal Green is a display accent — it fails WCAG contrast for body-size text
on white. Use it for the playhead, large headings, and UI accents; use Ink for text.

## Type

- **Wordmark**: JetBrains Mono Medium → `toolAssisted`; JetBrains Mono Bold in
  Signal Green → `.run`
- **UI/body text**: Inter; **code/technical contexts**: JetBrains Mono
- `logo.svg` has the wordmark converted to outlines; installing fonts is only
  needed to regenerate artwork (both families are in `~/.local/share/fonts` on
  the dev machine; render scripts live in the session scratchpad).

## Usage notes

- The wordmark is always lowercase-with-capital-A: **toolAssisted.run** — never
  "Tool Assisted Run" in the mark itself.
- The playhead stays Signal Green in all contexts; cells take the ink color of
  the surface (dark on light, light on dark).
- The input pattern (which cells are pressed) is part of the mark — don't
  rearrange it per use.
- The mark is built for motion: the natural animation is cells lighting up as
  they cross the playhead. Use sparingly (loading states, homepage hero).
- Small sizes: prefer 32px+ favicons; at 16px the grid abstracts to texture —
  acceptable, but don't shrink the full lockup below ~200px width.
