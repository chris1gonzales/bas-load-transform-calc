# BAS Transformer Load Calculator (PWA)

Static single-page app. No build step, no backend, no accounts.

Files: `index.html` (the app), `sw.js` (offline cache), `manifest.webmanifest`, icons, `netlify.toml`.

## Deploy
**Netlify (drag and drop):** Sites > Add new site > Deploy manually > drop this folder. Static only, so no function or Blobs usage.
**Netlify (from GitHub):** push to a repo, then Add new site > Import from Git. Publish directory `.`, no build command.
**GitHub Pages:** push to a repo, Settings > Pages > Deploy from branch `main` / root. Paths are relative so a project subpath works.

## Updating
Edit `index.html`, bump `VERSION` (in index.html, shown in the header) and `CACHE` in `sw.js`, redeploy. Installed copies pick up the new version on the next load after the new service worker activates.

Library data and sources: see the in-app "Library & sources" table and the NueralNet note "BAS Transformer Load Calculator".
