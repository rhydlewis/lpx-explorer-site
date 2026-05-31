# CLAUDE.md — lpx-explorer-site

Landing page for **LPX Explorer**, a free, open-source, read-only macOS app for
inspecting Logic Pro `.logicx` projects. The app repo is `rhydlewis/lpx-explorer`.

## What this repo is

A single self-contained `index.html` (inline CSS/JS). It fetches the latest
`.dmg` from the `rhydlewis/lpx-explorer` GitHub Releases API at runtime and
pulls the screenshot from that repo's raw URL. Fonts come from Google Fonts.

## Deploy setup

- **GitHub Pages**, deploying from `main` / root (no build step, no Actions).
- **Custom domain:** `lpxexplorer.app` (apex). Set via the `CNAME` file at repo
  root and the Pages API. DNS (apex A/AAAA records) is managed at the
  registrar, not here.
- Pages config is changed via `gh api repos/rhydlewis/lpx-explorer-site/pages`,
  not the Settings UI.
- "Enforce HTTPS" should stay on once the certificate has provisioned.

## Analytics

- **GoatCounter only** — cookieless, no consent banner needed. Endpoint:
  `https://lpx-explorer-app.goatcounter.com/count`, loaded just before
  `</body>`.
- No Google Analytics, no other trackers or scripts. Keep it that way.

## Content rules

- **British English** throughout (licence, colour, optimise, etc.).
- Direct, technical tone. State what the app does and how; no marketing fluff,
  no hype adjectives.
- Be honest about limitations (it's beta, parses an undocumented format, keep
  backups). The existing FAQ copy sets the register — match it.
