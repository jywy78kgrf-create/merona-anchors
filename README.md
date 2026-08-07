# merona anchors

Nightly SHA-256 integrity anchors for the [merona](https://merona.io)
x402 settlement index. Each line in `anchors.jsonl` fingerprints one day's
immutable snapshot before publication: the data stays private, but the hash
plus this repo's push timestamp proves data matching it existed on that date.
When datasets publish, hash them and compare.

The same hashes are attested nightly **on Base** via EAS by merona's
attester wallet:

    0x644678AD37833C0d52f0170f1F73A5e62Bc3e6d5

Browse them at
[base.easscan.org](https://base.easscan.org/address/0x644678AD37833C0d52f0170f1F73A5e62Bc3e6d5)
— each attestation's `combinedSha256` must equal the `combined_sha256` here,
byte for byte. Two independent ledgers, one hash: git proves the history,
consensus proves it from the day of attestation forward.

Only attestations from the address above are merona's. The wallet carries a
matching on-chain identity attestation pointing back at merona.io and this
repo, so the binding holds in both directions.

This repo is append-only and is never force-pushed.
