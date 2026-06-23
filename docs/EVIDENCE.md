# Evidence Ledger

Every row applies only to its named frozen fixture or workflow gate.
No row is a real-world accuracy percentage or a promise of complete audit coverage.

| Evidence | Status | Metrics |
|---|---|---|
| `architecture-v218` — Machine-enforced split-before-grow architecture budget | **PASS** | approved_debt=8 warnings; new_warnings=0 warnings |
| `batch-hardening-v214` — Batch msg.value relationship false-negative hardening | **PASS** | relationship_positives=3 cases; hard_negative_findings=0 findings; unexpected_cross_findings=0 findings |
| `calibration-v213` — Repository-unseen historical calibration records both success and failure | **MIXED** | transfer_successes=1 cases; documented_false_negatives=1 cases; patched_findings=0 findings |
| `foundation-v210f` — Offline self-contained tests and fail-closed quality gates | **PASS** | registered_detectors=20 detectors; foundation_tests=6 tests |
| `fresh-holdout-v217` — Fresh post-change holdout preserves a documented dispatch-helper miss | **MIXED** | transfer_successes=2 cases; documented_false_negatives=1 cases; patched_and_hard_negative_findings=0 findings |
| `historical-v212` — Source-faithful historical traceability with a clean patched control | **LIMITED** | vulnerable_target_findings=1 findings; patched_findings=0 findings; root_cause_rows=9 checks |
| `product-cli-v218` — Exact-scope product CLI is deterministic and source-free | **PASS** | unit_tests=72 tests; registered_detectors=20 detectors; full_source_files_exported=false boolean |
| `public-demo-v211` — Frozen public demo with positive and hard-negative controls | **PASS** | labeled_case_passes=29 cases; matched_findings=8 findings; clean_hard_negatives=21 cases |

## architecture-v218

- Category: `architecture`
- Source checkpoint: `config/anti_monolith_budget_v216.json and tools/anti_monolith_gate_v216.py`
- Metrics: approved_debt=8 warnings; new_warnings=0 warnings
- Limitation: Eight pre-existing review warnings remain approved debt; PASS means no new warning or growth beyond the frozen budget.

## batch-hardening-v214

- Category: `red-to-green`
- Source checkpoint: `docs/BATCH_PAYMENT_RELATIONSHIP_V214.md`
- Metrics: relationship_positives=3 cases; hard_negative_findings=0 findings; unexpected_cross_findings=0 findings
- Limitation: The change was designed from a known false-negative family, so it is regression and hardening evidence rather than independent discovery.

## calibration-v213

- Category: `curated-holdout`
- Source checkpoint: `docs/CALIBRATION_V213.md`
- Metrics: transfer_successes=1 cases; documented_false_negatives=1 cases; patched_findings=0 findings
- Limitation: The cases were curated after detector freeze, not randomly sampled or cryptographically blinded.

## foundation-v210f

- Category: `foundation`
- Source checkpoint: `docs/PRODUCT_VALIDATION.md and tools/foundation_gate_v210f.py`
- Metrics: registered_detectors=20 detectors; foundation_tests=6 tests
- Limitation: Foundation tests prove local contracts and determinism, not real-project vulnerability recall.

## fresh-holdout-v217

- Category: `curated-holdout`
- Source checkpoint: `docs/FRESH_HOLDOUT_V217.md`
- Metrics: transfer_successes=2 cases; documented_false_negatives=1 cases; patched_and_hard_negative_findings=0 findings
- Limitation: The holdout is curated and the unresolved DISPATCH_HELPER_DEPTH_ONE limitation remains open.

## historical-v212

- Category: `public-historical`
- Source checkpoint: `docs/HISTORICAL_CASE_V212.md`
- Metrics: vulnerable_target_findings=1 findings; patched_findings=0 findings; root_cause_rows=9 checks
- Limitation: The detector learned from this vulnerability family, so the case proves traceability and regression coverage only.

## product-cli-v218

- Category: `product-workflow`
- Source checkpoint: `docs/PRODUCT_CLI_V218.md`
- Metrics: unit_tests=72 tests; registered_detectors=20 detectors; full_source_files_exported=false boolean
- Limitation: Authorization is user-declared, and stable output does not establish autonomous-audit capability or customer value.

## public-demo-v211

- Category: `synthetic`
- Source checkpoint: `docs/PUBLIC_DEMO_V211.md`
- Metrics: labeled_case_passes=29 cases; matched_findings=8 findings; clean_hard_negatives=21 cases
- Limitation: Synthetic labeled fixtures are not a representative real-world benchmark and must not be reported as accuracy.

The underlying acceptance portfolio is `v2.1.9` and keeps all claim-boundary flags false.
