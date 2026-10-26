# Banner source

`banner.html` is the self-contained source of the README banner (`../banner-light.png` and `../banner-dark.png`). One file holds both themes: a `@media (prefers-color-scheme: dark)` block swaps the colours.

## Identity

- **Fonts:** **IBM Plex Sans** (light 300 headline with a semibold second line) and **IBM Plex Mono** (labels and the figure caption), loaded from Google Fonts.
- **Colours:** `#025471` marine teal and `#7bccb9` sea-glass mint (sampled from `assets/brand/logo.png`), `#06303f` ink, `#f7f9f8` pearl background and `#04202b` dark background.
- **Motif:** a lab-notebook page: ruled header and footer lines with study metadata, and a round microscope-style field showing particles drifting toward a mat of bacteria, captioned "Fig. 1 · Concept illustration, not data".
- The logo is loaded from `../../../assets/brand/logo.png` on a white tile.

## Re-render

From the repository root:

```bash
export CHROME_PATH="<path to a Chrome or Chromium binary>"
node render-html.mjs .github/assets/source/banner.html .github/assets/banner-light.png --scheme light
node render-html.mjs .github/assets/source/banner.html .github/assets/banner-dark.png --scheme dark
```

`render-html.mjs` is a small Playwright script (not in this repository) that opens the page at 1600 x 600, waits for fonts, and saves a 2x screenshot with the given `prefers-color-scheme`. Any headless browser that screenshots a 1600 x 600 viewport at 2x, once in light and once in dark mode, gives the same result.

## Notes for agents

- Keep the banner honest: no invented numbers, users, partners or results. Status words in the banner must match the README's "Honest status" section.
- Check both PNGs after rendering for overflow, clipped text and weak contrast.
