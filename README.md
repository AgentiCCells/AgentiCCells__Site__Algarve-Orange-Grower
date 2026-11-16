# Quinta do Sol Laranja (example site)

An example site, made up: a wholesale orange grower in the Algarve, with a simulated order workflow in English and Portuguese. There is no payment, nothing is sent and nothing is saved. Every farm detail, price and delivery rate is invented.

- Static files in `src/`: `index.html`, `style.css`, `app.js`, `data.js`. Open `src/index.html` in a browser; it works from a folder.
- To steer the site, edit `src/data.js` (notice, prices, varieties, delivery zones).
- To use it as a template, change the names, varieties, prices and zones in `data.js` and the text in `index.html`.
- Releases: every push to `dev` runs `.github/workflows/pages.yml`: Agent trailer check, build, validate, leak scan, deploy to GitHub Pages, then a tag. The version is v0.1.N, set by CI only (first release v0.1.0); it shows in the footer and at `/version.json`. Locally: `scripts/release.sh`.
- The same files live in an sgit vault (`.sg_vault/bare/` is its encrypted store, committed here; `.sg_vault/local/` holds keys and is never committed).
- Licences: code Apache-2.0 (see LICENSE), text and images CC BY 4.0.

Built by sites@AgentiCCells.dinis for Dinis Cruz, who plays the farmer. See hub.json.

## The vault

The same files are in sgit vault `797hd9f1`. The read key is public on purpose (it gives read access only; the write key is never in this repository):

- Browse: https://dev.vault.sgraph.ai/#sgit_public_read_a05ff747180cf9216621d654977a36245ddd48b8cbd8d66357c292f5fee37edd%3A797hd9f1
- Clone: `pip install sgit-ai` then `sgit clone sgit_public_read_a05ff747180cf9216621d654977a36245ddd48b8cbd8d66357c292f5fee37edd:797hd9f1`
