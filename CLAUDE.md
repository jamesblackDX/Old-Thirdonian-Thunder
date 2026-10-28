# Old Thirdonian Thunder website

Static single-page site for a Last Man Stands cricket team. No framework, no build step, no package.json.

## Structure

- index.html holds all HTML, CSS and JavaScript in one file. The club badge is embedded as a base64 data URI (it appears twice: homepage badge and header icon). Do not replace it with a file path, as the page must work as a standalone file.
- logo.png is used only as the favicon.
- Sections (home, squad, podcasts, fixtures, standings, honours, shop) are shown and hidden by JavaScript. Links use #squad, #podcasts, #fixtures, #standings, #honours and #shop. A click handler calls route() directly rather than relying on hashchange, so links work inside embedded previews. Keep it that way.
- Club content lives in six arrays near the bottom of the script, under the comment EDIT YOUR CLUB CONTENT HERE: SQUAD, PODCASTS, FIXTURES, STANDINGS, HONOURS, SHOP. HONOURS and SHOP start empty and show a placeholder message until filled in. Content edits should normally only touch these arrays.

## Design rules

- Black background with an animated lightning canvas behind everything.
- Club colours: teal #57b0a1 and gold #fcc125.
- Homepage: six buttons above the badge, as white boxes with dark bold sans-serif text and 5px rounded corners. No other colours for these buttons.
- Desktop menu: a set of cricket stumps (white, teal bands, gold bails) in the centre, with Meet the Squad, Podcasts and Fixtures & Results stacked on the left, and Standings, Roll of Honour and Club Shop on the right.
- Badge position: nudged right on all screen sizes so the shield's top point lines up with the centre of the buttons. On desktop it is centred in the space below the buttons, raised 20px.
- Mobile homepage (760px and narrower): no stumps; the buttons are two per row, with the badge sitting just below them rather than centred.
- Opening intro (homepage only, once per visit via sessionStorage): a cricket bat hits a white cricket ball (straight seam, not a baseball) at the screen, the screen cracks and the glass falls away to reveal the homepage. It plays even with reduced motion set, and a tap or key press skips it. Built with the Web Animations API, not CSS animations, so the reduced-motion CSS rule does not stop it.
- Page headings are white, in the same bold sans font as the player names.
- Squad cards show first name, bold surname, and an optional gold role label. Batting and bowling styles are deliberately not shown.
- Do not use player photos, logos or other images taken from the Last Man Stands website. Their terms do not allow reproduction.

## Writing style

British English. No em dashes.

## Deployment

GitHub repository connected to Cloudflare Pages. Framework preset: None. Build command: empty. Build output directory: /. Production branch: main. Every push to main deploys automatically.
