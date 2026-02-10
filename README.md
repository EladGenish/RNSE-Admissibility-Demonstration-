
# RNSE Admissibility Demonstration  
**Control Stability Under Regime Shift (Surface-Only Verification)**

This repository presents a replay-based admissibility demonstration comparing three controllers under identical conditions:

- Fixed PID  
- Auto-tuned PID  
- RNSE-mediated control  

The experiment evaluates whether admissibility survives a regime shift using **only externally visible artifacts**, without access to controller internals.

The focus is not performance optimization, but **bounded behavior and cost of maintaining admissibility under perturbation**.

---

## Summary of Result

Under identical noise, sensor deception, and a mid-run regime shift:

- Fixed PID violates admissibility bounds after the shift.
- Auto-tuned PID preserves performance via high realignment cost (frequent retuning and large control spikes).
- RNSE preserves admissibility with bounded state evolution and bounded realignment cost, without retuning or learning.

These claims are derived exclusively from replayable, surface-visible artifacts.

---

## What Is Being Verified

This repository evaluates **admissibility**, not optimality.

Specifically:
- Whether declared bounds remain respected under replay (**CVR**)
- How costly it is to keep those bounds respected (**RCI**)

No controller asserts a regime change internally.  
Regime shifts are inferred post-hoc from observable behavior under replay.

---

## License

© Elad Genish  
Released under **CC BY-NC-ND 4.0**.
