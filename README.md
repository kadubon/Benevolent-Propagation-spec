# A Pure Natural Theory of Benevolent Propagation (Static Spec v0.1)
[![Paper DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17136050.svg)](https://doi.org/10.5281/zenodo.17136050)
[![Repo DOI (concept)](https://zenodo.org/badge/DOI/10.5281/zenodo.17138320.svg)](https://doi.org/10.5281/zenodo.17138320)

**Status:** Static, implementation-free. No Q&A, no issue triage. Fork-and-go.

This repository fixes the *minimal* protocol needed for **independent human/AI implementers across disciplines** to
(1) measure the four floors (ε, L₀, D_min, λ_min),
(2) estimate front speeds and directional lower bounds,
(3) submit falsifiers (R1–R3) in a uniform JSON format.

- **No-Meta closure:** No external controller or meta-objective is assumed.
- **Sufficiency only:** Positive floors ⇒ speed floor / directional lower bounds / Wulff-type lower shape.
- **Order-only objective:** Use Blackwell-monotone functionals; CMI is a canonical representative.

## How to use (5 steps)
1. Read `SPEC.md` (normative core).
2. Pick a test from `EVALUATION.md`.
3. Follow `MEASUREMENTS.md` to estimate floors and front speed.
4. Produce a JSON via `reports/schema.json` (see `example_report.json`).
5. Publish in your fork. (Optional) Announce your refuter in your README.

## Governance & Support
- **Static.** This repo will not respond to questions or PRs. Fork to extend, cite the spec.
- **Refuters.** If you believe you found R1–R3, include full reproduction in your fork and mark it clearly.

## License
Apache-2.0 (see `LICENSE`). Copyright © 2025 K. Takahashi.

