# FBMFOR — Food Fraud Analysis

[![Open In Colab (Chemometrics)](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ggkuhnle/fbmfor-foodfraud/blob/main/notebooks/FBMFOR_Chemometrics_Analysis.ipynb)
[![Open In Colab (XRD)](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ggkuhnle/fbmfor-foodfraud/blob/main/notebooks/XRD_Starch_Analysis.ipynb)
[![Open In Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ggkuhnle/fbmfor-foodfraud/main?filepath=notebooks/FBMFOR_Chemometrics_Analysis.ipynb)
[![GitHub Pages](https://img.shields.io/badge/docs-GitHub%20Pages-blue)](https://ggkuhnle.github.io/fbmfor-foodfraud/)

Interactive analysis notebooks for the **MSc Food Technology and Quality Assurance** module on food fraud analysis at the University of Reading.

## Practicals

| Practical | Notebook | Method |
|-----------|----------|--------|
| **Chemometrics Workbook** | `FBMFOR_Chemometrics_Analysis.ipynb` | PCA, HCA, PLS-DA, OPLS-DA on NMR/FTIR spectral data |
| **XRD Starch Analysis** | `XRD_Starch_Analysis.ipynb` | Polymorph fingerprinting of starch samples; unknown identification |

## Chemometrics Workbook

Provides a complete pipeline for multivariate analysis of spectroscopic data (NMR, FTIR) in food authentication:

| Method | Type | Purpose |
|--------|------|---------|
| **PCA** | Unsupervised | Exploratory analysis, outlier detection, variance structure |
| **HCA** | Unsupervised | Hierarchical clustering, dendrogram visualisation |
| **PLS-DA** | Supervised | Classification with cross-validation, VIP scores |
| **OPLS-DA** | Supervised | Orthogonal signal correction, S-plot biomarker identification |

Preprocessing options include baseline correction (ALS), normalisation (SNV, area, min-max), and Savitzky-Golay derivatives.

## XRD Starch Analysis

Guides students through XRD polymorph fingerprinting of five starch types (Corn, Wheat, Potato, Tapioca, Unknown). Covers waterfall plots, automated peak detection and assignment, relative crystallinity estimation, and identification of an unknown sample — with a food fraud context.

## Quick Start

1. Click an **Open in Colab** badge above
2. Run the cells sequentially — the chemometrics notebook loads a demo dataset automatically; the XRD notebook fetches `data/xrd.csv` directly from GitHub
3. To use your own data in the chemometrics notebook, uncomment the upload cells in Section 3

## Data Format

### Chemometrics Workbook

The notebook expects **two CSV files**:

**Spectral data** (`spectra.csv`):

| Sample_ID | 4000.0 | 3997.8 | ... | 400.0 |
|-----------|--------|--------|-----|-------|
| EVOO_01   | 0.032  | 0.028  | ... | 0.015 |
| ROO_01    | 0.041  | 0.035  | ... | 0.018 |

**Metadata** (`metadata.csv`):

| Sample_ID | Class |
|-----------|-------|
| EVOO_01   | EVOO  |
| ROO_01    | ROO   |

### XRD Starch Analysis

A single merged CSV (`data/xrd.csv`) with columns `TwoTheta, Counts, Starch`.

## Repository Structure

```
├── notebooks/
│   ├── FBMFOR_Chemometrics_Analysis.ipynb   # Chemometrics practical
│   └── XRD_Starch_Analysis.ipynb            # XRD starch practical
├── data/
│   └── xrd.csv                              # XRD dataset (Corn, Potato, Tapioca, Wheat, Unknown)
├── index.qmd                                # Quarto landing page (→ GitHub Pages)
├── _quarto.yml                              # Quarto project configuration
├── styles.css                               # Custom styling for the site
├── .github/
│   └── workflows/
│       └── publish.yml                      # GitHub Actions workflow for Pages
├── .nojekyll                                # Bypass Jekyll on GitHub Pages
└── README.md                                # This file
```

## GitHub Pages Site

The documentation site is built with [Quarto](https://quarto.org) and deployed automatically via GitHub Actions. It provides an overview of the notebooks, links to Colab, and guidance for students.

### Setup (one-time, for the repository owner)

1. Push this repository to GitHub
2. Go to **Settings → Pages → Source** and select **GitHub Actions**
3. The site will build and deploy automatically on each push to `main`

## Dependencies

All dependencies are available in Google Colab by default:

- numpy, pandas, scipy
- scikit-learn
- plotly
- matplotlib

## References

- Trygg, J. & Wold, S. (2002). Orthogonal projections to latent structures (O-PLS). *J. Chemometrics*, 16(3), 119–128.
- Barker, M. & Rayens, W. (2003). Partial least squares for discrimination. *J. Chemometrics*, 17(3), 166–173.
- Eilers, P.H.C. & Boelens, H.F.M. (2005). Baseline correction with asymmetric least squares smoothing.
- Zobel, H.F. (1988). Molecules to granules: a comprehensive starch review. *Starch*, 40(2), 44–50.
- Imberty, A. et al. (1991). The double-helical nature of the crystalline part of A-starch. *J. Mol. Biol.*, 201, 365–378.

## Licence

This material is provided for educational use within the University of Reading MSc programme.

## Contact

**Gunter Kuhnle**
Department of Food and Nutritional Sciences, University of Reading
g.g.kuhnle@reading.ac.uk
