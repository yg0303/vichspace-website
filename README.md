# VichSpace Café & Co-Working — website

Static website (plain HTML/CSS/JS, no build step).

## Pages
- `index.html` — Home: scroll-controlled walk-in (frames in `/frames`), MacBook screens (About, Drinks, Food, Desserts, Space), reviews, footer
- `menu.html` — Interactive menu (Hot, Iced, Frappé & Soda, Food, Desserts). Deep links: `menu.html#iced`, `#food`, etc.
- `space.html` — Co-working floor, meeting rooms, café gallery

## Folders
- `frames/` — 142 frames of the walk-in video (scrubbed on scroll)
- `photos/` — menu photos (one per item)
- `img/` — logo, interior, meeting rooms, map, MacBook shot

## Deploy free on Cloudflare Pages (no GitHub needed)
1. Sign in at https://dash.cloudflare.com (free account).
2. Go to **Workers & Pages → Create → Pages → Upload assets** ("Direct Upload").
3. Name the project, e.g. `vichspace` → your site will be at `https://vichspace.pages.dev`.
4. Drag in this whole folder (or the zip) and click **Deploy**.
5. To update later: open the project → **Create deployment** → upload the folder again.

## Deploy from GitHub instead (auto-deploy on every push)
1. Create an empty GitHub repo, e.g. `vichspace-website`.
2. In this folder:  `git remote add origin https://github.com/<you>/vichspace-website.git && git push -u origin main`
3. Cloudflare: **Workers & Pages → Create → Pages → Connect to Git** → pick the repo.
   Framework preset: **None**. Build command: *(leave empty)*. Build output directory: `/`.

## Use your own domain later
Project → **Custom domains** → add `vichspace.co` (the domain's DNS must be on Cloudflare, or add the CNAME it shows you).

## To do
- Replace the walk-in frames with the cinematic Artlist video when it's ready
- Live Google reviews (Places API) — needs a Google Cloud API key
- Photos for Hokkaido Tiramisu Cheesecake and Iced Black Tea
