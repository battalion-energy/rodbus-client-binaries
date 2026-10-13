# rodbus-client

Prebuilt static Linux binaries for
[`rodbus-client`](https://github.com/stepfunc/rodbus).

Each GitHub Release includes:

- `x86_64-unknown-linux-musl`
- `aarch64-unknown-linux-musl`
- `SHA256SUMS`

This repository checks the latest stable upstream release weekly. A newly
detected upstream version is published under its exact upstream tag, such as
`v1.5.0`.

Each commit pushed to `main` rebuilds the current upstream version and publishes
the next local revision, such as `v1.5.0-r1` and `v1.5.0-r2`. This keeps the
latest release download URL current while retaining the upstream version in the
release tag.

Pull requests that modify [`.github/workflows/`](.github/workflows/) build both
targets and create the release archives for validation, but never publish a
release.
