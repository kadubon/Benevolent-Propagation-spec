# Measurements (Minimal, Auditable Recipes)

## Floors
- **ε (visibility / Doeblin):** Estimate via minorization tests (Nummelin splitting / coupling-from-the-past).
  Report: lower confidence bound on ε (e.g., 95% CI lower end).
- **L₀ (contraction / SDPI/LSI):** Inject a nuisance channel N and measure decay `I_t / I_0 ≈ (1−L₀)^t`.
  Report: fitted `L₀` and CI from bootstrap over runs.
- **D_min (transport):** Lower-bound via commute time / spectral gap / Cheeger-type conductance on the substrate graph or manifold.
  Report: `D_min` lower bound with method tag.
- **λ_min (gain):** Evaluate derivative of `E[u_{t+Δt} − u_t | u≪1] / u_t` at zero density.
  Report: local linear fit slope at small `u`.

## Front speed (α-level)
- Fix `α ∈ (0,1)` (default `α=0.5`). Track the α-level set position `x_α(t)`.
- Estimate `v_*` by robust regression on large `t`; report slope and CI; include window size and outlier policy.

## Directional bounds
- Compute effective `D(u)` and `λ_lin(u)` along direction `u` (principal axis or great-circle ray).
- Estimate penalty `Λ_+(u)` from barrier/heterogeneity metrics; ensure **coarse-graining monotonicity** check is logged.

## Reporting
- Fill `reports/example_report.json` template and conform to `reports/schema.json`.
- Include seeds, version hashes, and any coarse-graining operator used.
