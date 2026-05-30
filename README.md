# Neon Drift

A self-contained JavaScript arcade game built with HTML canvas.

## Play

The public GitHub Pages build should be available at:

https://imjusttestingit.github.io/neon-drift/

You can also open `index.html` directly in a browser.

## Controls

- Move with WASD, arrow keys, mouse, or touch.
- Hold Space, Shift, mouse, or touch for overdrive.
- Collect prism shards, pass through gates, and avoid drones.
- Open the hidden admin panel with `#admin` in the URL or `Ctrl` + `Shift` + `A`.

## Admin secret

The admin passphrase is not committed to the repository. Set a GitHub Actions
repository secret named `NEON_DRIFT_ADMIN_SECRET`, then run the Pages workflow.
The deploy step publishes only a SHA-256 hash to `admin-config.js`.

Because this is a static GitHub Pages game, the admin panel is suitable for
local game controls and lightweight moderation settings. Do not put truly
sensitive server-side powers behind this client-only panel.

## Files

- `index.html`: complete game, styles, and JavaScript.
- `admin.js`: hidden admin panel and game-control UI.
- `.github/workflows/pages.yml`: GitHub Pages deployment workflow.
- `.nojekyll`: serves the static game files exactly as written.
