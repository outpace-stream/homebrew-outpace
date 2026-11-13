# Repository guidelines

Use main as the base and feat/, fix/, docs/, test/ or chore/ topic branches. Never force-push main.
Keep manifests pinned to published engine releases and verify their checksums against SHA256SUMS.
Never commit real AceStream content ids, infohashes or stream names, private captures, secrets or local state.
The engine release generator lives in outpace-stream/outpace-engine at tools/release/package_manifests.py.
Run the shared identifier check from outpace-stream/actions before publishing changes (CI runs it
as outpace-stream/actions/identifier-hygiene@v1):
curl -fsSL https://raw.githubusercontent.com/outpace-stream/actions/v1/identifier-hygiene/check_identifiers.py | python3 -
