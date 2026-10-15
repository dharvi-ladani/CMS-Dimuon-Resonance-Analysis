# CMS Dimuon Resonance Analysis

A particle-physics data analysis project using CMS Open Data to reconstruct dimuon invariant-mass spectra, study resonance peaks, and investigate fitting and detector-related systematic effects.

## Project Overview

This project studies the invariant mass of oppositely charged muon pairs in CMS 2012 proton-proton collision data. The analysis investigates prominent resonances, including J/ψ, ψ(2S), the ϒ family, and the Z boson.

The workflow covers data exploration, dimuon reconstruction, resonance fitting, systematic variations, and detector studies.

## Objectives

- Explore the dimuon invariant-mass distribution.
- Reconstruct opposite-sign muon pairs and calculate their invariant masses.
- Fit resonance peaks using signal and background models.
- Investigate the sensitivity of fitted results to fit-window and selection variations.
- Study transverse-momentum and pseudorapidity distributions.
- Compare results from the Run2012B and Run2012C datasets.
- Document analysis limitations and potential detector-related effects.

## Analysis Workflow

### 1. Data Exploration

Notebook: `01_data_exploration.ipynb`

Initial exploration of the available data, distributions, and relevant variables.

### 2. Dimuon Reconstruction

Notebook: `02_dimuon_reconstruction.ipynb`

Reconstruction of opposite-sign muon pairs and calculation of their invariant masses.

### 3. Resonance Fitting

Notebook: `03_resonance_fitting.ipynb`

Construction of invariant-mass histograms and fitting of resonance peaks using signal and background parameterisations. Fitted parameters are used to characterise the resonances.

### 4. Systematics and Detector Studies

Notebook: `03b_systematics_and_detector_studies.ipynb`

Study of fit-window and selection variations, transverse momentum and pseudorapidity distributions, toy closure tests, and comparison between Run2012B and Run2012C.

## Key Results

Populate this section using the final saved outputs from the notebooks.

| Quantity | Result |
|---|---|
| Run2012B events processed | 29,308,627 |
| Opposite-sign pairs in the high-pT diagnostic | 37,621,109 |
| Pairs with pair pT above 10 TeV | 1,823 |
| Pairs outside the pT bins across the three histogram regions | 130 |

Add a separate table containing the fitted resonance masses, statistical uncertainties, and evaluated systematic uncertainties from the final resonance-fitting results.

## High-Transverse-Momentum Diagnostic

A diagnostic identified 1,823 of 37,621,109 opposite-sign pairs with pair transverse momentum above 10 TeV. Such values are unphysical for 8 TeV proton-proton collisions and are consistent with pathological reconstructed tracks or badly measured track curvature.

Of the high-pT pairs, 130 lie in the three histogram regions: 1 in the J/ψ and ψ(2S) region, 9 in the ϒ region, and 120 in the Z region. These pairs appear in the nominal histograms but are excluded from the pT-binned histograms. Their overall fraction of the entries in the three histogram regions is approximately 0.0013%.

## Limitations

- No muon reconstruction efficiency or detector acceptance correction has been applied.
- No momentum-scale calibration has been applied; fitted masses are not precision measurements.
- Simplified signal and background models may introduce fit-shape biases.
- Only the fit-window and selection variations explicitly evaluated are included in the systematic uncertainties.
- Multiple opposite-sign pairs can originate from the same event; event-level correlations are not explicitly modelled.
- No dedicated trigger-efficiency or trigger-bias study has been performed.
- The high-pT diagnostic identifies pathological reconstructed pairs, but their underlying causes have not been investigated further.

## Tools and Technologies

- Python
- Jupyter Notebook / Google Colab
- NumPy
- Pandas
- Matplotlib
- SciPy and other fitting libraries actually used in the notebooks
- CMS Open Data

## Repository Structure

```text
Cern-Dimuon-Analysis/
├── 01_data_exploration.ipynb
├── 02_dimuon_reconstruction.ipynb
├── 03_resonance_fitting.ipynb
├── 03b_systematics_and_detector_studies.ipynb
├── figures/
├── requirements.txt
└── README.md
```

The `figures/` directory and `requirements.txt` should be included if created.

## Reproducibility

The notebooks are designed for an interactive Python notebook environment such as Google Colab. Run the notebooks in sequence, ensuring that the required datasets and dependencies are available.

Dataset access, input paths, and dependency versions should be documented before reproducing the complete analysis.

## Acknowledgements

This project uses CMS Open Data for educational and research-oriented data analysis.
