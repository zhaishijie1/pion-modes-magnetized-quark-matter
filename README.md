# Numerical data

**Manuscript:** *Neutral and Charged Pion Modes in Magnetized Quark Matter with Chiral Imbalance*  
**arXiv:** https://arxiv.org/abs/2611.28838

This repository contains the numerical CSV data supporting the manuscript. The files provide the NJL-model results used for the numerical curves and tables. All temperatures, energies, and masses are given in GeV; the magnetic-field variable `eB` is given in GeV².

## Vacuum reference and normalization

The manuscript uses the neutral-pion vacuum pole mass

\[
m_{\pi^0}^{\mathrm{vac}} = 0.134\;\mathrm{GeV},
\]

defined in the model at \(T=B=\mu_5=0\). This is the model vacuum pole mass used for the normalization in Fig. 3.

The file `neutral_pion_mass_magnetic_field_T0.csv` stores the unnormalized pole mass \(m_{\pi^0}\). To reproduce Fig. 3, calculate

\[
\frac{m_{\pi^0}}{m_{\pi^0}^{\mathrm{vac}}}
=
\frac{\texttt{m\_pi0\_GeV}}{0.134\;\mathrm{GeV}}.
\]

## Files

- `quark_mass_temperature.csv` — constituent quark mass versus temperature at `eB = 1 GeV²`, for `mu5 = 0, 0.05, 0.10, 0.15, 0.20 GeV`. Columns: `T_GeV`, `eB_GeV2`, `mu5_GeV`, `M_minus_m0_GeV`, and `M_constituent_GeV`. The latter includes the current quark mass `m0 = 0.005 GeV`; `M_minus_m0_GeV` is the tabulated component before adding `m0`.

- `neutral_pion_mass_temperature.csv` — neutral-pion pole mass versus temperature at `eB = 1.0` and `0.4 GeV²`, for `mu5 = 0.05, 0.10, 0.15, 0.20 GeV`. Columns: `T_GeV`, `eB_GeV2`, `mu5_GeV`, and `m_pi0_GeV`.

- `neutral_pion_mass_magnetic_field_T0.csv` — unnormalized neutral-pion pole mass versus `eB` at `T = 0`, for `mu5 = 0, 0.05, 0.10, 0.15, 0.20 GeV`. Columns: `eB_GeV2`, `T_GeV`, `mu5_GeV`, and `m_pi0_GeV`. Divide `m_pi0_GeV` by `0.134` to obtain the normalized quantity plotted in Fig. 3.

- `charged_pion_inverse_propagator.csv` — real part of the inverse charged-pion propagator, \(\operatorname{Re}\mathcal{F}_{\pi^+}(\omega)\), in the lowest mesonic Ritus channel at `eB = 1 GeV²`, `mu5 = 0.20 GeV`, and `q3 = 0`, for `T = 0, 0.18, 0.25 GeV`. Columns: `omega_GeV`, `T_GeV`, `eB_GeV2`, `mu5_GeV`, `q3_GeV`, and `Re_inverse_propagator_F_pi_plus`.

- `charged_pion_mass_temperature.csv` — selected positive-energy real-axis solutions defining the charged-pion mass in the lowest mesonic Ritus channel at `eB = 1 GeV²`, for `mu5 = 0, 0.05, 0.10, 0.15, 0.20 GeV`. The mass is evaluated at `q3 = 0`. Columns: `T_GeV`, `eB_GeV2`, `mu5_GeV`, `m_pi_plus_GeV`, `segment_id`, and `source_status`. The `segment_id` distinguishes separate displayed solution segments. Entries recorded as `Null` in the source are retained as empty values with `source_status = Null_in_source`.

- `charged_pion_Unitary_threshold_temperature.csv` — lowest physical quark-antiquark Unitary threshold versus temperature at `eB = 1 GeV²`, for the same five values of `mu5` used in the charged-pion temperature scan. Columns: `T_GeV`, `eB_GeV2`, `mu5_GeV`, and `lowest_physical_Unitary_threshold_GeV`.

- `charged_pion_mass_magnetic_field_T0.csv` — charged-pion mass versus `eB` at `T = 0`, for `mu5 = 0, 0.05, 0.10, 0.15, 0.20 GeV`. Columns: `eB_GeV2`, `T_GeV`, `mu5_GeV`, and `m_pi_plus_GeV`. This file contains the NJL-model results only.

## Figure-to-file correspondence

| Manuscript figure | Data source |
|---|---|
| Fig. 1 — constituent quark mass versus temperature | `quark_mass_temperature.csv` |
| Fig. 2 — neutral-pion mass versus temperature | `neutral_pion_mass_temperature.csv` |
| Fig. 3 — normalized neutral-pion mass versus magnetic field | `neutral_pion_mass_magnetic_field_T0.csv`; divide the mass by `0.134 GeV` |
| Fig. 4 — schematic analytic structure of the charged-pion cuts | Schematic figure; no numerical CSV file is required |
| Fig. 5 — real inverse charged-pion propagator | `charged_pion_inverse_propagator.csv` |
| Fig. 6 — charged-pion mass and lowest Unitary threshold at `mu5 = 0` | `charged_pion_mass_temperature.csv` and `charged_pion_Unitary_threshold_temperature.csv` |
| Fig. 7 — charged-pion mass and lowest Unitary threshold at finite `mu5` | `charged_pion_mass_temperature.csv` and `charged_pion_Unitary_threshold_temperature.csv` |
| Fig. 8 — charged-pion mass versus magnetic field | `charged_pion_mass_magnetic_field_T0.csv` |

The lattice-QCD points displayed in Fig. 8 are taken from Ref. [Ding2026] and are not included in this repository. The CSV file for Fig. 8 contains the NJL-model curves only.

## Notes for reading the data

- The suffixes `_GeV` and `_GeV2` indicate the units of the corresponding columns.
