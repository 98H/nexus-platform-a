# Spec Kit Constitution: Platform A

## Product Intent
Enterprise software system built autonomously with Nexus Agent Graph.

## Architectural Invariants
- Zero Blast-Radius: Isolated sandbox execution per task.
- Strict TDD: BDD acceptance tests frozen before code development.
- Clean Code & Deterministic Verification: Sole oracle is test runner exit code == 0.
