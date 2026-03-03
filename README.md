# iOS Binary Size Reduction Skill

Staged, security-aware iOS binary size reduction guidance for production Swift/Xcode projects.

## What this is

- Runs on three risk tiers (`low`, `balanced`, `aggressive`) to minimize surprise.
- Enforces safety gates before moving to the next tier.
- Tracks impact on size, security posture, and behavior/performance risk.

The implementation is the skill:

- `skills/ios-binary-size-reduction/SKILL.md`

## Why this makes sense

Binary growth in iOS apps usually clusters in a few areas: compiler output, linker output, symbols/metadata, assets, and dependency bloat. A staged workflow improves predictability by forcing measurable wins and gating risk at each pass.

## Install

```bash
npx skills add ehmo/ios-binary-size-reduction
```

(For Claude plugin users, install via the `.claude-plugin/marketplace.json` included in this repo.)

## Contributing (Pull Requests)

- Fork the repository and create a feature branch from the default branch.
- Keep PRs scoped to one change set (for example one risk-tier behavior tweak or one documentation correction).
- When behavior changes are made, update:
  - `skills/ios-binary-size-reduction/SKILL.md`
  - any usage examples or notes in this README
- Run a quick pass over changed text and examples for consistency and path accuracy.
- In the PR description include:
  - what changed,
  - why the change improves safety or size outcomes,
  - and any observed risk trade-offs.
- PR titles should stay focused and clear (`feat: ...`, `fix: ...`, `docs: ...`).

Example PR checklist:

- [ ] Scope matches the PR title
- [ ] Workflow steps and risk tiers remain consistent
- [ ] No stale references in `package.json` or install docs
- [ ] README remains aligned with the current skill behavior

## Repo structure

```text
ios-binary-size-reduction/
├── README.md
├── LICENSE
├── package.json
├── .claude-plugin/
│   └── marketplace.json
└── skills/
    └── ios-binary-size-reduction/
        └── SKILL.md
```

## Sources used by the skill

- Apple Xcode build settings reference
- Xcode app-thinning and export guidance
- App Store build size constraints
- Swift compiler optimization guidance (`-Osize`)

These sources are referenced in the skill file for context and follow-up.
