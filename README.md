# soapps-legal

Static legal pages for SoApps applications, served by GitHub Pages.

Separate from the app repositories on purpose: a privacy policy has to stay
reachable at a stable URL for as long as the app is installed, which is a
different lifecycle from the code, and it must be public while an app
repository need not be.

## Live addresses

| Page | URL |
|---|---|
| Foundation Match — privacy policy | `https://ochicoineau-sys.github.io/soapps-legal/foundation-match/privacy/` |
| Foundation Match — terms of use | `https://ochicoineau-sys.github.io/soapps-legal/foundation-match/terms/` |

The privacy URL is the one Google Play requires in the store listing, and it is
compiled into the app, so **it must not move**. If it ever has to, the app has
to be rebuilt and resubmitted.

## Rules for anything added here

Every page asserts in its own text that it carries no trackers, no analytics
and no external fonts. That has to stay true, so:

- single self-contained HTML file per page — no build step, no framework
- **no analytics, no cookies, no consent banner**
- **no external fonts** — system font stack only
- no external CSS, JS, images or iframes
- responsive and dark-mode aware on its own

`.nojekyll` at the root stops GitHub Pages running a Jekyll build, so the tree
is served exactly as committed and no theme assets are injected.

## Source of truth

The pages are authored in the Foundation Match repository at
`foundation-match/docs/public/` and copied here. Edit them there, then copy —
so the wording stays next to the code whose behaviour it describes and can be
audited against it.

## Publishing

Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder
`/ (root)`.
