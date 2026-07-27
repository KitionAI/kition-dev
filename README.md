# Kition Developer Downloads

This public repository hosts release automation and versioned Kition runtime
binaries for local client development and desktop packaging. Runtime source
code is never stored in this repository.

## Downloads

Use the [Releases](https://github.com/KitionAI/kition-dev/releases) page to
download the runtime version pinned by the Kition client. Each release provides
platform archives, a manifest, checksums, provenance metadata, and binary SBOMs.

The Kition desktop installers for end users are published separately in the
[Kition releases](https://github.com/KitionAI/kition/releases).

Runtime binaries are governed by the `RUNTIME-LICENSE.txt` file included in
each platform archive.

## Release automation

The `Build Runtime Release Assets` workflow checks out the private
`KitionAI/kition-runtime` repository with a read-only deploy key, validates the
selected source revision, and builds signed runtime archives for macOS arm64,
macOS x64, Windows x64, and Linux x64. Only verified binary release artifacts
leave the private source checkout.

Maintainers dispatch the complete guarded release flow from `KitionAI/kition`
with `pnpm release:github <version>`.
