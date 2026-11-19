# PATTERN_ADOPTION

Relationship to the WyattAu pattern canon
([pattern-standards](https://github.com/WyattAu/pattern-standards)),
validated by `scripts/adoption-check.py`. Evidence paths are relative to
this repo root.

| Pattern | Status | Evidence |
|---|---|---|
| T13 | adopted | src/lib.rs:40 (`LinkGraph` is an in-memory typed structure; no I/O, threads, or effects, hosts own the imperative shell) |
| P64 | planned | property suite for `hop_neighbors` invariants (depth monotonicity, origin exclusion, shallowest-path retention), target 2027-Q1 |

## Omitted patterns

T46 (fixed-point Datalog) and T28 (content-addressed Merkle DAGs) were
evaluated for this crate and omitted: queries are direct BFS calls over
caller-owned string ids, with no rule engine and no hashing
(references/adoption-format.md rule 6; R6: no named failure mode, no
adoption).
