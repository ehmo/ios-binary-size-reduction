# Changelog

## Unreleased
- Internal cleanup and instruction tightening pass is tracked in the latest commit.

## v1.0.2 - 2026-03-03
- Added deterministic, reproducible build execution model:
  - Added exact `xcodebuild` templates for workspace/project and archive/export flow.
  - Enforced release-only clean archive comparison with no-debug artifact reuse.
- Improved validation discipline:
  - Added double-run/median gate rule and noise-floor re-run handling.
  - Added run/pass timing metadata and `pass_status` in output schema.
- Reduced risk ambiguity:
  - Added per-target scope for settings.
  - Required two-run stability before Tier 3 and blocked `P14+` by default for low risk.
- Hardened reflection-risk controls with explicit verification checklist.

## v1.0.1 - 2026-03-03
- Refined guardrails in `SKILL.md`:
  - Replaced unsafe-safety-flag guidance with explicit disallowed compiler flags.
  - Added reproducible baseline metadata requirements and pre-edit no-op control.
- Improved pass and technique traceability:
  - Standardized staged pass IDs to `P1..P20` across scheduler and catalog.
- Added concrete gate thresholds and stricter rollback criteria.
- Expanded output schema with env metadata, cumulative size deltas, and rollback flags.

## v1.0.0 - Initial
- Added initial `ios-binary-size-reduction` skill with staged low/balanced/aggressive workflow, gates, and evaluation schema.
