# Teknologia arjessani – TOTA

Static single-page site (`index.html` + `assets/`) for the TOTA project ("Teknologia, Osallisuus, Toimintakyky, Asiakaslähtöisyys"). No build step, no framework — just edit `index.html` and the image files in `assets/` directly.

## Deployment

Deployed via [Coolify](https://coolify.dev.roboai.fi) (RoboAI team instance):

- Coolify resource: `teknologiakartoitus` (Static build strategy, nixpacks staticfile provider, served by `nginx:alpine`)
- Live URL: https://teknologiakartoitus.dev.roboai.fi
- A GitHub webhook triggers an automatic Coolify deployment on every push to `main` — no manual deploy step needed.

To update the live site: edit `index.html` / `assets/`, commit, and push to `main`. Coolify picks it up automatically (deployment log visible in Coolify under the application's "Deployment Logs" tab, usually finishes in about a minute).

Do not confuse this Coolify resource with the unrelated `Tarkistuslista` application on the same Coolify instance (different project, domain `tarkistuslista.dev.roboai.fi`).
