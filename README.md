# Old Thirdonian Thunder

Website for Old Thirdonian Thunder Cricket Club.

This is a plain HTML site with no build step. It is hosted on Cloudflare Pages, which publishes the site automatically each time a change is pushed to the main branch.

## Files

- index.html: the whole site, including the homepage, Meet the Squad, Podcasts, Fixtures & Results, Standings, Roll of Honour and Club Shop. The club badge is built into this file, so it works on its own.
- logo.png: the club badge, used as the browser tab icon.

## Updating content

Open index.html and find the section marked EDIT YOUR CLUB CONTENT HERE near the bottom. It holds six lists:

- SQUAD: player names in display order, with an optional gold label (role) such as Captain.
- PODCASTS: episode title, date, description, length and link.
- FIXTURES: upcoming matches and results. Results include both scores, a summary and a scorecard link.
- STANDINGS: the Maidstone Boundary Bash table. It sorts itself by points, then net run rate.
- HONOURS: Roll of Honour entries, newest first: season, honour and optional details.
- SHOP: Club Shop items: name, price, optional description and a link to buy (leave the link empty until it is on sale).

Commit the change and the live site updates within a minute or two.
