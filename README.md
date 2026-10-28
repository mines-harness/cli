# Mines CLI releases

<p><img src="https://raw.githubusercontent.com/mines-harness/macos/main/assets/mines/icon-256.png" width="80" height="80" alt="Mines" /></p>

Release archives for the Mines command-line app and headless host. Run your coding agents on the computer that owns the workspace, then connect from an approved Mines client.

[Shared source](https://github.com/mines-harness/macos) · [Desktop](https://github.com/mines-harness/macos) · [Mobile](https://github.com/mines-harness/android)

New desktop and host builds are published together in [unified Mines releases](https://github.com/mines-harness/macos/releases). This repository retains earlier standalone host archives.

## Download earlier CLI releases

Download the archive for your operating system and architecture from [Releases](https://github.com/mines-harness/cli/releases). Each release includes `SHA256SUMS` for its published archives. Compare the checksum before running a download.

```sh
# Linux
sha256sum mines-<version>-linux-x64.tar.gz

# macOS
shasum -a 256 mines-<version>-darwin-arm64.tar.gz
```

Extract the archive and run the `mines` executable inside it. The archive includes its runtime; a separate Node.js installation is not required.

```sh
./mines --help
./mines serve --no-browser
```

If a Mines host already runs in the background, use its existing instance rather than starting another. Manage the account on that host with:

```sh
mines account login --no-browser
mines account status
mines devices list
```

Use the same `--base-dir` for commands when the host has a custom data directory. Runtime updates preserve your separate Mines data directory and account sign-in.

The Mines desktop client can use this release repository to install or update its remote command-line host over SSH. Your projects and provider credentials stay on that host.

## Repository contents

This repository distributes earlier release archives and checksums. Current shared source and the unified release pipeline live in [mines-harness/macos](https://github.com/mines-harness/macos). Runtime archives are attached to releases rather than committed to Git.

## Licenses

Mines is based on [T3 Code](https://github.com/pingdotgg/t3code). Its MIT license is retained in [LICENSE](LICENSE). Bundled components retain their own licenses; see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) and the notices included in each archive.
