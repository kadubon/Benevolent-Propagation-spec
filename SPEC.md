# Normative Core (Static Spec v0.1)

## 0. Scope
This is a *pure*, implementation-free specification of benevolent propagation under **no-meta closure**.
It fixes only (i) the assumptions, (ii) the measurable floors, and (iii) the guaranteed lower bounds.

## 1. Assumptions
- **Medium:** Metric-measure space with a measure-preserving ergodic group action (ℤ^d or ℝ^d).
- **No-meta closure:** Dynamics via local Markov kernels measurable on bounded neighborhoods; no external controller.
- **Mixing/regeneration:** Finite-range or summable mixing; ε>0 supplies renewal times.
- **Linearization-from-below:** At low density, `E[Δu] ≥ D_min Δ u + λ_min u` (operator Δ per transport).

## 2. Floors (intrinsic, measurable)
- **ε > 0** — visibility / Doeblin head (refresh / minorization)
- **L₀ > 0** — contraction floor (SDPI/LSI constant)
- **D_min > 0** — minimal effective diffusivity / conductance
- **λ_min > 0** — minimal linearized local gain around zero density

*Terminology map:* ε≡Doeblin head; L₀≡SDPI/LSI; D_min≡minimal conductance; λ_min≡zero-density linear gain.

## 3. Order-only objective
Admissible functionals are Blackwell-coherent and coarse-graining monotone; any two such functionals induce the same
preference *order* up to positive affine transforms. **CMI** is a canonical representative.

## 4. Guarantees (sufficiency)
- **Isotropic speed floor:** `v_* ≥ 2√(D_min λ_min)`.
- **Directional lower bounds:** For direction `u`,
  `v_*(u) ≥ [ 2√(D(u) λ_lin(u)) − Λ_+(u) ]_+`,
  where `Λ_+(u)` is a directional penalty (heterogeneity/barrier cost) that is **monotone non-increasing** under symmetric Markov coarse-graining.
- **Wulff-type lower shape:** If `inf_u v_*(u) > 0`, rescaled occupied sets contain a deterministic Wulff crystal in the limit.

## 5. Falsifiers (R1–R3)
- **R1.** Stationary ergodic medium with `ess-inf(D_min, λ_min) > 0` but `liminf` front speed `= 0`.
- **R2.** A *symmetric* coarse-graining that strictly **increases** `Λ_+(u)`.
- **R3.** Renewal present (ε>0) yet persistent failure of linear growth not explained by floor vanishing.

## 6. Scope boundary
This spec does **not** prescribe algorithms, controllers, or design choices. It only states **sufficient conditions** and how to **measure** them.
