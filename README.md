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


## v1.4.0
- Adds a Belimo 24 V actuator picker (section 2, "+ Add Belimo actuator") and a Belimo selector that fills "Actuator VA each" in section 4.
- Data: `belimo-devices-v1.1.0.js` (275 models) from the Belimo 2026 US Product Guide & Price List. VA is the transformer-sizing figure; running/holding W shown in the row note. Lines are marked "any".
- Not listed (no VA in the catalog, not guessed): NR, GR, GK-R, TR24, TFRB24, LRX/ARX MFT, AFRX, globe-valve actuators, EV/EPIV -E actuators, UP/120/230 V models, and dual actuator/heater values. Enter nameplate VA manually for those.
- Updating: when editing, also bump `CACHE` in sw.js; belimo-devices-v1.1.0.js is in the cache list.
