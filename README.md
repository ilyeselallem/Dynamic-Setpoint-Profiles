# PLC Dynamic Ramp Generator for Steam Sterilizers

A professional, scan-time-independent dynamic setpoint generator (`FB_TempRamp_Gen`) for Siemens S7-1200 PLCs, developed in TIA Portal using SCL. 

Designed for thermal processes like autoclaves and steam sterilizers to prevent thermal shock and PID loop overshoot by smoothing heating and cooling trajectories.

---

## Features
* **Deterministic Execution:** Runs inside a dedicated Cyclic Interrupt (`OB30` at 100ms) to eliminate scan-time jitter.
* **Floating-Point Precision:** Uses `REAL` data types to prevent stair-step quantization errors.
* **Bi-Directional:** Automatically handles both heating and cooling ramps based on signed rate calculations.
* **Asymptotic Clamping:** Locks precisely onto the target temperature upon completion.
