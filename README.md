# amie-updates

Release + auto-update feed for **AMIE** (WaveDivision Audio).

This repository hosts the GitHub Releases that the AMIE desktop app's Tauri
updater polls. Each release carries the signed `*.app.tar.gz` + `.sig`, the
`.dmg`, and per-platform `latest-*.json` manifests. On **release publish**, the
*Merge Update Manifests* workflow merges them into a single `latest.json`, which
the app fetches from:

```
https://github.com/WaveDivision-Audio/amie-updates/releases/latest/download/latest.json
```

Releases are produced from the app repo via `npm run release`. Do not commit app
source here — this repo only hosts release artifacts and the merge workflow.
