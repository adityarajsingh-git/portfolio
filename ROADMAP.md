# Roadmap

Single-page portfolio (`index.html`, no build step). Gate: `npx --yes html-validate index.html`.

## Accessibility
- [ ] Keyboard user can skip the nav and jump straight to the main content (skip link + `<main>` landmark).
- [ ] Theme toggle exposes its state (`aria-pressed`) and the label reflects the current theme.
- [ ] Modal traps focus, closes on Esc and returns focus to the trigger.
- [ ] Marquee and typed text pause for users with `prefers-reduced-motion` (verify existing handling).
- [ ] Nav link for the section in view is marked `aria-current`.

## Sharing / SEO
- [ ] Sharing the link shows a title, description and image preview (Open Graph + Twitter tags). (owner: needs preview image)
- [ ] Browser UI colour matches the theme (`theme-color`).
- [ ] Search engines get a canonical URL. (owner: final domain)

## Reliability / performance
- [ ] Page renders with readable fallback fonts when Google Fonts fails to load.
- [ ] Below-the-fold images lazy-load and have explicit width/height (no layout shift).
- [ ] Page works with JavaScript disabled (reveal sections are visible without JS).

## Content
- [ ] Resume download shows file size/format in the label.
- [ ] 404 page that links back home. (owner: hosting)

## Shipped
- Dark/light theme with persisted choice
- Résumé download
- Project "ship it" modal, 3D showcase, reduced-motion media query
- html-validate gate config
