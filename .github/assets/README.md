# README images

Images used by the root `README.md`.

| File | What it is | How it was made |
| --- | --- | --- |
| `banner-light.png`, `banner-dark.png` | README banner for light and dark mode | Rendered from [`source/banner.html`](source/banner.html) with headless Chrome (26 October 2026), using `assets/brand/logo.png` |
| `how-it-worked.svg` | Five-step summary of the study | Hand-written SVG in the README palette (marine teal, mint, IBM Plex Sans with system fallbacks); the text summarises the final presentation |

The hero image is the existing conceptual cover in `assets/brand/cover.png` (AI-generated, not a product photo).

This repository has no running software, so there are no app screenshots. Images here must only show public or synthetic content; never add interview, survey or personal details to them.

## Visual identity

Dental, clinical and research brands favour sober type, teal and white, and lots of space. The banner reads like a research document because the project is a study, and it repeats "not clinically validated" in the header.

- **Fonts:** **IBM Plex Sans** (light 300 headline with a semibold second line) and **IBM Plex Mono** (labels and the figure caption).
- **Colours:** `#025471` marine teal and `#7bccb9` sea-glass mint (sampled from `assets/brand/logo.png`), `#06303f` ink, `#f7f9f8` pearl background and `#04202b` dark background.
- **Motif:** a lab-notebook page: ruled header and footer lines with study metadata, and a round microscope-style field showing particles drifting toward a mat of bacteria, captioned "Fig. 1 · Concept illustration, not data".

The README badges use the same colours. To change the banner, edit [`source/banner.html`](source/banner.html) and follow [`source/README.md`](source/README.md) to re-render both PNGs.
