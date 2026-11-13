# KETO GUYS

A cheeky 70-second carnivore arcade game. Single static page, no build step.
Satire only. Not nutrition advice.

## Files
- `index.html` the whole game (HTML, CSS, JS inline)
- `_headers` lets the page use the camera for hand tracking (Cloudflare Pages)

## Deploy on Cloudflare Pages
1. Push these files to a GitHub repo.
2. Cloudflare dashboard > Workers & Pages > Create > Pages > Connect to Git.
3. Pick the repo. Framework preset: None. Build command: leave empty. Build output directory: `/`.
4. Save and Deploy. Add a custom domain under the project's Custom domains tab if you want one.

## Notes
- Hand tracking uses MediaPipe, loaded from jsDelivr and Google storage. It needs HTTPS and camera permission; if either fails the game falls back to touch.
- The leaderboard is stored per device (localStorage) plus a Copy Score button. A shared board needs a backend (for example Cloudflare KV or D1 behind a Pages Function).
