# Numa · integrity anchors

**Numa** is an independent measurement index. Its datasets are captured in
immutable daily snapshots that are not yet public.

Each line of `anchors.jsonl` contains the SHA-256 digest of one day's snapshot
files (and a combined digest), published here so that GitHub's public commit
timestamps attest **when that data existed** — without revealing anything about
its contents.

When the datasets are published, anyone can verify them against these anchors:

```
sha256sum <snapshot files>   # must match files_sha256 for that date
```

A hash proves existence and integrity; it discloses nothing. Anchors are
append-only and are pushed nightly by an automated job.
