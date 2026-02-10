
# Methods: Admissibility Verification Under Replay

## Evaluation Principle

This work adopts a **surface-only admissibility framework**.  
All conclusions must survive adversarial replay using only externally visible artifacts.

Controller internals are explicitly out of scope.

---

## Constraint-Violation Residual (CVR)

CVR measures whether declared admissibility bounds are violated under replay.

Violations are derived from observable divergence, oscillatory growth, or unbounded control effort.

---

## Realignment Cost Integral (RCI)

RCI measures the cumulative cost required to restore admissibility once perturbed.

RCI is instantiated as a weighted combination of:
- Integrated control effort
- Frequency of correction events (retuning or admissibility clamps)

No universal weighting is assumed.
