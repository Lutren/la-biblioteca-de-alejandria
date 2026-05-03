# Observacionismo For Local-First AI Agents

## Summary

Observacionismo is a practical control layer for AI agents that can use tools.
It asks a simple question before action:

> What evidence, receptor, witness log and rollback path exist for this action?

The goal is not to make agents magical. The goal is to make agent work
inspectable enough that a human or another agent can pause it, replay it, hand
it off, or reject it.

## Why Newton

Newton is useful here as a metaphor for compression. Newtonian mechanics is not
"false" in the regimes where it works; it is a strong local approximation. A
good agent safety system should behave the same way:

- use simple local rules when the evidence is enough;
- escalate to richer models when residue rises;
- keep the conditions of validity visible;
- never confuse a useful approximation with total truth.

This is the public-safe version of the Newton hook:

> Newton is a local compression. Observacionismo is a method for keeping the
> compression label attached.

That framing matters for AI because hallucinations often happen when a system
forgets the regime where a claim is valid. The practical fix is not a grand
theory. The practical fix is evidence, provenance, uncertainty, receptors,
falsifiers and witness logs.

## The Core Loop

1. Observe the action request.
2. Classify risk and reversibility.
3. Attach sources, tool checks and self-checks.
4. Route high-impact actions through an authorized receptor.
5. Decide `APPROVE`, `REVIEW` or `BLOCK`.
6. Write a witness log so the action can be audited later.

## What This Solves

- Destructive tool calls without backup proof.
- Public claims without sources.
- Long-running coding sessions with poor handoff.
- Release decisions without secret scans or license checks.
- Research hypotheses presented as validated truth.

## What This Does Not Claim

- No proof of consciousness.
- No validated new physics.
- No medical or therapeutic claim.
- No guarantee of autonomous agent safety.
- No claim that synthetic benchmarks equal production calibration.

## Canonical Repos

- `obsai-core`: core evidence and action-gate primitives.
- `safe-exec`: practical wrapper for tool execution.
- `agent-handoff-protocol`: practical handoff workflow.
- `residueos`: dashboard/API direction.
- `duat-genesis` and `duat-lab`: synthetic falsifier labs.

## Research Note: Psi Hypothesis

The private research language sometimes uses a Psi hypothesis:

> observed reality can be modeled as an update process before it is represented
> as geometry, force, trajectory or measurement.

Publicly, this belongs in falsifiable labs only. A useful public implementation
does not say "Psi is true." It says:

- this model reproduces Newton in this regime;
- this model reproduces Einstein in this regime;
- this model fails these tests;
- this model makes this different prediction.

That is why the public repos emphasize tests, benchmarks and witness logs
instead of claims of final truth.

## Next Evidence Targets

- 100-500 action scenarios: no gate vs gate.
- Metrics: errors prevented, false blocks, correct allows, human review cost and
  time overhead.
- Reproducible demos for common agent frameworks.
- A public replay example: requested action, decision, witness log and final
  report.
