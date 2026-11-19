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
- [x] Below-the-fold images lazy-load and have explicit width/height (already shipped: the only image is the above-the-fold avatar, which has width/height; lazy-loading it would hurt LCP).
- [x] Page works with JavaScript disabled (already shipped: reveal hiding is scoped to `html.js`).

## Content
- [x] Resume download shows file size/format in the label ("Résumé ↓ (PDF, N KB)"; size is hardcoded, update when resume.pdf changes).
- [ ] 404 page that links back home. (owner: hosting)

## Polish (added in refresh)
- [x] Native scrollbars and form controls follow the active theme (`color-scheme`).
- [ ] Section anchor jumps land with the heading clear of the sticky nav (`scroll-margin-top`).
- [ ] User can copy the contact email with one click and gets "Copied" feedback.
- [ ] Printing the page produces a clean, light, single-column layout (print stylesheet hides aurora/3D/nav).
- [ ] External links that open a new tab say so to screen readers (visually hidden "(opens in new tab)").
- [ ] `<noscript>` note is not needed (page already works without JS), but the typed hero line has a static fallback when JS is off.
- [ ] Footer year is not hardcoded stale text. (owner: decide whether to automate)

## Shipped
- Dark/light theme with persisted choice
- Résumé download
- Project "ship it" modal, 3D showcase, reduced-motion media query
- html-validate gate config
