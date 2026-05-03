# Contributing

Contributions are welcome when they make the public layer easier to test,
understand or falsify.

## Good Contributions

- New synthetic benchmark scenarios.
- Clearer README examples.
- Framework adapters for public APIs only.
- Reproducible witness-log demos.
- Tests that catch unsafe approvals or unnecessary blocks.

## Required Boundaries

- Use synthetic data.
- Do not include private prompts, sessions, keys, RPG/TCG material, books or
  local workspace paths.
- Label thresholds as `DEMO_ONLY` unless a calibration report exists.
- Keep claims narrow: evidence gates, witness logs, handoff, review and
  falsifiability.

## Scenario Format

Useful benchmark scenarios should include:

- action request;
- expected decision: `APPROVE`, `REVIEW` or `BLOCK`;
- evidence supplied;
- risk class;
- why the expected decision is correct;
- whether human review cost is acceptable.
