# victorheringer.github.io

Static site built with Hugo (theme `hugo-bearblog`) and run locally via Docker.

## Requirements

- Docker Desktop
- Docker Compose (`docker compose`)

## Run locally

The `docker-compose.yml` is configured to run the Hugo server with drafts enabled (`-D`).

1. Start the server:

   - `docker compose up`

2. Open:

   - http://localhost:1313/

To stop it, press `Ctrl + C` in the terminal.

## Build (generate static site)

The Hugo build outputs files into `docs/` (configured via `publishDir`) to simplify GitHub Pages hosting.

- Production build:

  - `docker compose run --rm hugo --minify`

- Build including drafts (optional):
  - `docker compose run --rm hugo -D --minify`

## Publish to GitHub Pages

This repository uses the “Deploy from a branch” method, pointing GitHub Pages to the `docs/` folder on the `main` branch.

1. Build the site:
   - `docker compose run --rm hugo --minify`
2. Commit/push the `docs/` folder:
   - `git add docs`
   - `git commit -m "Build site"`
   - `git push origin main`
3. On GitHub, go to **Settings → Pages**:
   - **Source**: _Deploy from a branch_
   - **Branch**: `main`
   - **Folder**: `/docs`

Note: set `baseURL` in `config.yaml` to your final site domain.
