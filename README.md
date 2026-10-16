# Idle Slayer Companion compatibility hosting

This repository hosts a reviewed static snapshot at `/idle-slayer-companion/` and the previous-address launcher at `/idle-slayer-ascension-map/`. The launcher forwards recognized links without analytics and provides a read-only offline map/export fallback. Both addresses use the same origin so existing browser storage can remain available.

The application source, game-data provenance, licenses, and rollout instructions are maintained in [Idle Slayer Companion](https://github.com/AustinGarrod/idle-slayer-companion). `release.json` identifies the reviewed source commit and release; `SHA256SUMS` binds every deployed file. GitHub Actions verifies these bytes before publishing only `site/`.

To refresh, build and validate the source release, run `yarn prepare:migration`, replace the two reviewed directories from `.cache/site-migration`, regenerate the checksum manifest and release metadata, and review the complete artifact before publishing. Preserve unrelated future user-site content and keep the old-address bridge available. Do not copy saves, private inputs, development tools, or credentials here.

Project Pages for `idle-slayer-companion` may serve the current application while this user site retains the same-origin bridge and complete fallback snapshot. Never publish an old-base rollback artifact at the new Companion path. No worker is registered at the user-site root.
