# Copilot instructions for KlasLab

## Project overview
- KlasLab is a static, single‑page marketing site built as one HTML file with inline CSS and a small amount of inline JS in [index.html](KlasLab/index.html).
- Styling is custom, with Bootstrap 5.3.3 loaded from CDN for grid/components (no local build step) in [index.html](KlasLab/index.html#L1-L120).
- Assets (logos/photos) are referenced directly from assets/img; keep filenames and paths stable in [index.html](KlasLab/index.html#L120).

## Structure & patterns
- Theme tokens live as CSS variables prefixed with `--kl-` in the `:root` block; adjust colors, spacing, and shadows there first in [index.html](KlasLab/index.html#L16-L60).
- Section layout uses `.kl-band` variants and card styles (`.kl-card`, `.kl-surface`) defined in the same inline `<style>` block in [index.html](KlasLab/index.html#L150-L320).
- CTA buttons consistently use the `.btn-accent` class; keep CTA styles aligned there in [index.html](KlasLab/index.html#L60-L90).
- In‑page navigation relies on section `id`s and a custom scroll offset for CTA anchors; update anchor ids and scroll logic together in [index.html](KlasLab/index.html#L535-L571).
- The floating “back to top” button is rendered in HTML and toggled in JS; ensure the `#btn-scroll-top` id stays in sync with the script in [index.html](KlasLab/index.html#L573-L587).
- The footer year is injected via JS; keep the `#year` span id when editing the footer in [index.html](KlasLab/index.html#L535-L544).

## Developer workflow
- No build or test tooling; edit [index.html](KlasLab/index.html) directly and open it in a browser for preview.
- Custom domain for static hosting is configured via [CNAME](KlasLab/CNAME) (GitHub Pages style).

## Cross‑project consistency
- Visual measurements and spacing mirror KarperLab (“match KarperLab measurements/feel” comment), so keep the KlasLab theme consistent when adjusting core spacing variables in [index.html](KlasLab/index.html#L16-L30).
