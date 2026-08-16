# CLAUDE.md

Working notes for this repo. Read [PROJECT.md](PROJECT.md) first — it maps the
structure, architecture and conventions.

## Git workflow

**Always commit and push directly to `main`.** Do not create or use sub-branches
unless explicitly instructed otherwise.

```bash
git add -A && git commit -m "..." && git push origin main
```

## Priorities, in order

1. Fast
2. Lightweight
3. Responsive
4. Agile and reliable on weak/slow Wi-Fi
5. Visually polished

Avoid unnecessary dependencies, assets, requests and code. Visual quality and
animation are the acceptable tradeoffs for extra weight — keep them optimized
and intentional. Everything else earns its bytes.

## House rules

- Static site, no build step. Edit the shipped files directly.
- Adding or changing inventory/parts copy means editing `assets/js/data.js`,
  not the HTML.
- Any user-visible string needs both `es` and `en`; Spanish is the default.
- Colors come from the CSS custom properties — never hardcode one in a
  component rule, or dark mode breaks.
- Bump the `?v=N` cache-buster on every page whenever CSS or JS changes.
- Ship images as WebP in `assets/img/`, sized for their real display size, with
  `width`/`height` attributes set. Keep the PNG original in `Images/`.
- Header markup is duplicated across `index.html`, `bikes.html` and
  `parts.html` — change all three together.
- Update `PROJECT.md` when the structure or behaviour meaningfully changes.
