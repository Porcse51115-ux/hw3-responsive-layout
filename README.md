# Portfolio Site — Matt Sheaffer

Personal portfolio site (Home, Projects, About/Contact) built with semantic HTML, responsive CSS (Flexbox + Grid), and accessible form design.

## Accessibility Fixes (WAVE)

1. **Contrast error fixed** — Changed link color from `#b5651d` (4.33:1 ratio) to `#8b4513` (5.66:1 ratio) to meet WCAG AA's 4.5:1 minimum against the `#f5f5f0` background.
2. **Redundant link removed** — Removed the duplicate "About/Contact page" link on the home page since the nav already links to the same URL, reducing noise for screen reader users.
3. **Skip navigation link added** — Added a hidden "Skip to main content" link at the top of every page so keyboard and screen reader users can bypass the nav and jump directly to page content.

## Gestalt Principles

1. **Proximity** — Project cards on the Home and Projects pages are grouped tightly together inside a CSS Grid container with consistent `24px` gaps, visually communicating that TruckOps AI, CrimeCast Studio, and Voss Studio belong to the same category (Featured Work) without needing an extra label on each one.
2. **Similarity** — All project cards share the same white background, border radius, and amber left-border accent. This consistent visual treatment signals that each card is the same type of content, so users understand immediately that they're browsing a set of related items.

## Contact Form (About/Contact page)

- Every input has a matching `<label>` element linked by `for`/`id`.
- Inputs are wrapped in a `<fieldset>` with a `<legend>` ("Send a Message") to group them semantically.
- Required fields use `aria-required="true"` and display inline error messages via `role="alert"` spans linked with `aria-describedby`.
- Invalid fields receive `aria-invalid="true"` and a visible red border on validation failure.
