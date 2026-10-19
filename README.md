# NTG Companion Releases

This public repository hosts the signed release artifacts for the Not That Genius Windows companion. The source repository stays private.

- Latest portable build: <https://github.com/wooooooooooook/not-that-genius-release/releases/latest>
- Signed update feed: <https://github.com/wooooooooooook/not-that-genius-release/releases/latest/download/latest-portable.json>

Each release contains the portable ZIP, its detached Ed25519 signature, and the signed `latest-portable.json` manifest. The app verifies the manifest signature and the ZIP hash before installing an update.

This repository contains release artifacts only. It is created and populated by the `Desktop Release` workflow in the source repository and by `npm run desktop:publish:github`.
