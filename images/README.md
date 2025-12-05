Blueprint logo images

This folder currently contains `blueprint_logo.png` (base raster image).

To make the logo render crisply on high pixel-density (Retina) displays, provide higher-resolution versions with the following naming convention used by the site:

- `blueprint_logo.png` (1x, required) — baseline image
- `blueprint_logo@2x.png` (2x) — double resolution for 2x displays
- `blueprint_logo@3x.png` (3x) — triple resolution for 3x displays

Alternatively, prefer a vector SVG for perfect scaling across densities:
- `blueprint_logo.svg` — best option if available; replace the `img` `src` and `srcset` accordingly.

How the HTML uses these files (already implemented in `index.html`):

<img src="images/blueprint_logo.png" alt="Blueprint logo" srcset="images/blueprint_logo.png 1x, images/blueprint_logo@2x.png 2x, images/blueprint_logo@3x.png 3x">

Notes:
- Provide exact pixel-doubled/tripled versions (e.g., if the 1x image is 45×50 px, the @2x should be 90×100 px).
- If you supply only @2x or @3x versions, the browser will fallback to the available entries in the `srcset`.
- For background images in CSS, you can use `image-set()` or `-webkit-image-set()`.

If you want, I can generate placeholder @2x/@3x copies now (they will be duplicates of the existing PNG), or you can supply proper high-resolution assets.
