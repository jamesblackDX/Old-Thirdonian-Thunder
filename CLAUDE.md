# Old Thirdonian Thunder website

Static single-page site for a Last Man Stands cricket team. No framework, no build step, no package.json.

## Structure

- index.html holds all HTML, CSS and JavaScript in one file. The club badge is embedded as a base64 data URI (it appears twice: homepage badge and header icon). Do not replace it with a file path, as the page must work as a standalone file.
- logo.png is used only as the favicon.
- Sections (home, squad, podcasts, fixtures, standings) are shown and hidden by JavaScript. Links use #squad, #podcasts, #fixtures and #standings. A click handler calls route() directly rather than relying on hashchange, so links work inside embedded previews. Keep it that way.
- Club content lives in four arrays near the bottom of the script, under the comment EDIT YOUR CLUB CONTENT HERE: SQUAD, PODCASTS, FIXTURES, STANDINGS. Content edits should normally only touch these arrays.

## Design rules

- Black background with an animated lightning canvas behind everything.
- Club colours: teal #57b0a1 and gold #fcc125.
- Homepage: four white, bold, underlined sans-serif links above the centred badge. No coloured buttons.
- Page headings are white, in the same bold sans font as the player names.
- Squad cards show first name, bold surname, and an optional gold role label. Batting and bowling styles are deliberately not shown.
- Do not use player photos, logos or other images taken from the Last Man Stands website. Their terms do not allow reproduction.

## Writing style

British English. No em dashes.

## Deployment

GitHub repository connected to Cloudflare Pages. Framework preset: None. Build command: empty. Build output directory: /. Production branch: main. Every push to main deploys automatically.
