# Outpace Homebrew tap

Install published [Outpace engine](https://github.com/outpace-stream/outpace-engine) binaries.

```bash
brew tap outpace-stream/outpace
brew install outpace-stream/outpace/outpace
brew services start outpace # optional
```

On macOS and Linux, `brew services` runs `outpace serve` bound to localhost.
To migrate from the old tap, stop its service if running, uninstall its outpace formula,
run `brew untap jamezrin/outpace`, then install from this tap and restart the service.

## Updating

The manifest is generated from published engine release `SHA256SUMS`; never guess a checksum.
From an engine checkout, run `tools/release/package_manifests.py` with explicit
`--homebrew-root` and `--scoop-root` checkout directories, then open a PR here.
See the [release guide](https://github.com/outpace-stream/outpace-engine/wiki/Releases-and-Versions#updating-the-homebrew-formula-and-scoop-manifest).
Installation is checked on the native platform in GitHub Actions.
