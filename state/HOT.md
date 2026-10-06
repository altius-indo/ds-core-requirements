# DS-CORE project state

## Now
- Baseline approved: 49 requirements (REQ-0001..0049), 11 decisions (DEC-0001..0011), 17 research findings (RF-0001..0017).
- Plan in place: 5 components, 11 epics, 36 stories, 48 tasks, 70 evals; trace gate PASS (100% requirement and criteria coverage).
- Semantic trace review 2026-10-06 scored 0.81; all 15 weak eval links fixed in CS-0006.
- In progress: TASK-0001 Rust workspace and CI skeleton; TASK-0003 Raft/range design; TASK-0009 transaction protocol design; TASK-0015 GQL conformance scope.
- No code repository exists yet; component paths (server/, importer/, harness/, operator/, drivers/) are placeholders and verification shows 0/94 criteria verified.

## Next
- Create the code repository and run TASK-0001: Cargo.toml workspace with server/, importer/, harness/ and rust-toolchain.toml; then point COMP-0001..0005 at the real paths.

## Watch
- Open decisions to record as DECs: transaction timestamp source TSO vs HLC (TASK-0009), client transport (TASK-0017), how a query is marked analytical (TASK-0024), operator language (assumed Go), minimum Linux kernel/glibc and Rust MSRV.
- PO-unconfirmed thresholds: failover 10 s, 99.99% availability, RPO 5 min / 7-day PITR, 10% HTAP degradation, 30-day erasure, 16 MiB property limit, one-hop 20 ms, 10M-edge supernodes, import 50k elements/s, operator ready in 10 min.
- Five findings graded THIN (RF-0009, RF-0010, RF-0015, RF-0016, RF-0017) need re-verification before external commitments.
- Coverage waivers for 6 non-applicable taxonomy cells are not yet in reqforge.json.
- Jepsen-style and 30-minute performance evals should run nightly, not per commit, when /reqforge:cicd generates the pipeline.

Last reconciled: 2026-10-06
