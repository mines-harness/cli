# Release archives

Only runtime archives and their SHA-256 checksums are published here. Each release identifies the Mines version, available platforms, and any installation or compatibility notes.

Every archive contains a self-contained `mines` executable, the local web client, required runtime dependencies, and license notices. Application state, account sessions, provider credentials, build source maps, and development configuration are excluded.

Before upload, release archives are checked for unexpected files, source maps, private machine paths, and credential patterns. Checksums are calculated from the final uploaded archives.

`SHA256SUMS` lists one SHA-256 digest and archive filename per line. On Linux, download that file alongside the archives and run `sha256sum --check SHA256SUMS`; on macOS, run `shasum -a 256 --check SHA256SUMS`.
