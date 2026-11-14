# Roadmap

Single-page portfolio (`index.html`, no build step). Gate: `npx --yes html-validate index.html`.

## Accessibility
- [x] Keyboard user can skip the nav and jump straight to the main content (skip link + `<main>` landmark).
- [x] Theme toggle exposes its state (`aria-pressed`, fixed label "Dark theme"; pressed = dark).
- [x] Modal traps focus, closes on Esc and returns focus to the trigger.
- [x] Marquee and typed text pause for users with `prefers-reduced-motion` (already shipped).
- [x] Nav link for the section in view is marked `aria-current`.

## Sharing / SEO
- [ ] Sharing the link shows a title, description and image preview (Open Graph + Twitter tags). (owner: needs preview image)
- [x] Browser UI colour matches the theme (`theme-color`, follows the toggle).
- [ ] Search engines get a canonical URL. (owner: final domain)

## Reliability / performance
- [x] Page renders with readable system fallback fonts when Google Fonts fails to load (fallback stacks on `--disp`, `--body`, `--mono`).
- [ ] Below-the-fold images lazy-load and have explicit width/height (no layout shift).
- [x] Page works with JavaScript disabled (already shipped: reveal hiding is scoped to `html.js`).

## Content
- [ ] Resume download shows file size/format in the label.
- [ ] 404 page that links back home. (owner: hosting)

## Shipped
- Dark/light theme with persisted choice
- Résumé download
- Project "ship it" modal, 3D showcase, reduced-motion media query
- html-validate gate config
