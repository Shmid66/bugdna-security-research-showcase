# Architecture Boundary

BugDNA is maintained as a modular monolith with a hard split-before-grow rule.

```text
exact authorized scope
  -> fail-closed manifest verification
  -> parsing and bounded analysis
  -> independent detector registry
  -> scoring and evidence ranking
  -> human validation
  -> deterministic source-free report bundle
```

## Ownership rules

- Detectors identify one narrow smell and do not own scope loading, reporting, proof execution, or submission.
- Product orchestration does not absorb parsing or detector logic.
- Reporting renders deterministic artifacts and does not search for vulnerabilities.
- CLI modules remain thin adapters.
- New functionality must fit explicit file caps and may not introduce a new architecture warning.

## Publication boundary

The `bugdna-security-research-showcase` showcase is a presentation layer only. It is generated from validated metadata and does not contain the private implementation.
