# merona · integrity anchors

**merona** is an independent, open measurement index for x402 / agentic-commerce
settlement. Each day's snapshot of the dataset is captured immutably, and its
SHA-256 digest is committed here **before** the numbers are published.

Each line of `anchors.jsonl` carries the SHA-256 digest of one day's snapshot
files (plus a combined digest). GitHub's public commit timestamps then attest
**when that data existed** — proof we can't quietly backdate or rewrite our own
history — without the anchor itself revealing anything about the contents.

Anyone can verify a published snapshot against its anchor:

    sha256sum <snapshot files>   # must match files_sha256 for that date

A hash proves existence and integrity; it discloses nothing on its own. Anchors
are append-only and pushed nightly by an automated job. The datasets themselves
live in the main repo: github.com/jywy78kgrf-create/merona
