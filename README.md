# Veristead

**Fail-closed evidence tooling for AI-era software verification.**

When AI systems write code and proofs, the expensive question stops
being *can the work be done* and becomes *what does the finished work
actually establish*. A proof can pass the checker and hold nothing. A
green result can be a claim nobody verified. An agent can grind at an
impossible task rather than say so. Veristead builds the tooling that
makes these failures visible, mechanical, and cheap to catch — on the
principle that every gate should refuse rather than pass by omission,
and every claim should ship with evidence a stranger can check.

## Projects

| Project | What it does | Status |
|---|---|---|
| **[verihalt](https://github.com/veristead/verihalt)** | Benchmark measuring whether AI models recognize *unprovable* proof obligations — certified walls, repeated draws, decision vs. articulation measured separately. | **Live.** 400 cells, 5 models, full dataset + instrument published. Paper in review. |
| **verikeep** | The conduct gate: a development-time discipline for AI agents writing verified code — human-owned claims, no escape hatches, escalation instead of silent workarounds. | Validated as verihalt's treatment arm; library packaging planned. |
| **verideed** | The evidence format: a signed, machine-checkable certificate stating what a verified artifact proves, assumes, and deliberately does not claim. | In development; specification and reference tooling, fall 2026. |
| **verigrip** | The relevance gate: mutation-based checks that a proof actually *grips* the code it claims to verify — a passing proof that survives broken code proved nothing. | In design; feasibility spike in progress. |

## How they fit together

The **keep** governs the producer's conduct. The **grip** tests
whether the produced proofs hold anything. The **deed** carries the
evidence across the trust boundary to people who weren't in the room.
The **halt** measures whether the models themselves know their
limits. Any piece stands alone; together they cover the path from an
agent's first edit to a stranger's informed trust.

## Principles

- **Fail closed.** A check that cannot run, cannot read its input, or
  finds its input missing refuses — it never passes by omission.
- **Evidence over assertion.** Results carry provenance: request IDs,
  pinned tool versions, content hashes, reproducible builds. Claims
  without receipts don't ship.
- **Watched failing first.** No gate is trusted green until it has
  been seen refusing a planted violation.
- **Honest scope.** What is *not* proven, *not* claimed, and *not*
  measured is stated as plainly as what is. Smaller true claims beat
  larger impressive ones.

These aren't aspirations; they're the operating record. verihalt's
repository documents its own instrument catching its authors —
including a benchmark item refuted by the models under test, credited
and reclassified in public.

## Contact

Issues and discussion on the individual project repositories.
