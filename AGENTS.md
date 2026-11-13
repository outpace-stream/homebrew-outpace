# Repository guidelines

Use main as the base and feat/, fix/, docs/, test/ or chore/ topic branches. Never force-push main.
Keep manifests pinned to published engine releases and verify their checksums against SHA256SUMS.
Never commit real AceStream content ids, infohashes or stream names, private captures, secrets or local state.
The engine release generator lives in outpace-stream/outpace-engine at tools/release/package_manifests.py.
Run python3 tools/hygiene/check_identifiers.py before publishing changes.
