# Numerical data

**Manuscript:** *Neutral and Charged Pion Modes in Magnetized Quark Matter with Chiral Imbalance*  
**arXiv:** https://arxiv.org/abs/2611.28838

This repository contains the numerical data supporting the manuscript. All masses and energies are given in GeV, and the magnetic-field variable `eB` is given in GeV².

## Vacuum reference

For reference, the experimental vacuum mass of the neutral pion is

$m_{\pi^0}^{\mathrm{vac}} \simeq 0.135\ \mathrm{GeV}$.


## Files

- `quark_mass_temperature.csv` — constituent quark mass versus temperature at `eB = 1 GeV²`, for `mu5 = 0, 0.05, 0.10, 0.15, 0.20 GeV`. `M_constituent_GeV` includes the current quark mass `m0 = 0.005 GeV`; `M_minus_m0_GeV` is the tabulated component before adding `m0`.

- `neutral_pion_mass_temperature.csv` — neutral-pion pole mass versus temperature at `eB = 1.0` and `0.4 GeV²`, for `mu5 = 0.05, 0.10, 0.15, 0.20 GeV`.

- `neutral_pion_mass_magnetic_field_T0.csv` — neutral-pion pole mass versus `eB` at `T = 0`, for `mu5 = 0, 0.05, 0.10, 0.15, 0.20 GeV`. The file contains the unnormalized NJL-model masses; the manuscript figure presents the mass normalized to its model vacuum value.

- `charged_pion_inverse_propagator.csv` — real part of the inverse charged-pion propagator in the lowest mesonic Ritus channel at `eB = 1 GeV²`, `mu5 = 0.20 GeV`, and `q3 = 0`, for `T = 0, 0.18, 0.25 GeV`.

- `charged_pion_mass_temperature.csv` — selected positive-energy real-axis solutions defining the charged-pion mass in the lowest charged-pion Ritus channel at `eB = 1 GeV²`, for `mu5 = 0, 0.05, 0.10, 0.15, 0.20 GeV`. The mass is evaluated at `q3 = 0`. `segment_id` distinguishes the displayed solution segments. Entries recorded as `Null` in the source are retained as empty values with `source_status = Null_in_source`.

- `charged_pion_Unitary_threshold_temperature.csv` — lowest physical quark-antiquark Unitary threshold versus temperature at `eB = 1 GeV²`, for the same five values of `mu5`.

- `charged_pion_mass_magnetic_field_T0.csv` — charged-pion mass versus `eB` at `T = 0`, for `mu5 = 0, 0.05, 0.10, 0.15, 0.20 GeV`.
