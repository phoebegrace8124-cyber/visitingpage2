# Visiting Page: [Facility Name]

A static HTML/CSS visiting guide for families and friends of people held at [Facility Name]. It is meant to live alongside The Remedy Project's site (https://www.theremedyproj.org) and borrows its look: dark navy background, white type, bold headlines, and highlighter-yellow accents.

The page layout follows the visiting guide at https://www.lahuelga.com/delaney: a "call first" alert, a sticky side menu that jumps to each section, and plain tables for the visiting schedule.

## What's in this folder

```
visiting-page/
├── index.html   Page content (all text lives here)
├── styles.css   All styling, with colors and fonts at the top
└── README.md    This file
```

No build step and no JavaScript. Open `index.html` in a browser to preview it.

## Fill in the content

Every `[Bracketed Text]` and example value is a placeholder. Search `index.html` for `[` and replace each one:

- Facility name, address, phone number, and map link
- Schedule tables in `#schedule` (copy one `.table-wrap` block per unit)
- Rules, special-visit email, property hours, directions
- Phone, video, and commissary app steps for your facility's providers
- Support organizations in `#support`

Please verify every hour, rule, phone number, and fee against the facility or its official site before publishing. People plan trips around this page, so wrong information costs them. Add the "effective" date and update it whenever the schedule changes.

## Match the live site's style

The colors and fonts at the top of `styles.css` are close approximations. I could only read the text of the Remedy Project pages, not their stylesheet, so they are not exact.

To get the real values:

1. Open https://www.theremedyproj.org/take-action in Chrome.
2. Right-click a headline and choose Inspect. In the Styles pane, find `font-family`, `color`, and `background-color`.
3. Copy those into the `:root` block in `styles.css` (`--ink`, `--paper`, `--marker`, `--font-display`, `--font-body`).
4. If their fonts are Google Fonts, update the `<link>` in `index.html`. If they are paid or custom fonts, ask the web team for permission and files, then add them with `@font-face`.

For the logo, ask the web team for the white logo file and replace the text `.brand` link with an `<img>` that has `alt="The Remedy Project"`.

## Publish

- **Their Webflow site:** Create a new page, add an Embed element, and paste the contents of `<body>` there. Paste the contents of `styles.css` into the page's custom code or a `<style>` tag. Webflow's own header and footer can replace the ones in this file.
- **Any static host (Netlify, GitHub Pages, Cloudflare Pages):** Upload the folder as is.
- **Own subdomain:** Host it as above and point something like `visit.theremedyproj.org` at it.

## Optional next steps

- **Other languages:** The reference page is multilingual. Copy `index.html` to `es/index.html` (and so on), translate it, set `<html lang="es">`, and link the versions to each other near the top of the page.
- **Safety note:** Include a short note about lawyer fraud, as the reference page does, if families you serve are at risk.
- **Images:** Add transit maps or entrance photos in an `images/` folder. Always include `alt` text.

## Accessibility

The page includes a skip link, visible keyboard focus, real `<table>` markup with captions, and reduced-motion support. Keep these when you edit. Check color contrast again if you change the palette.
