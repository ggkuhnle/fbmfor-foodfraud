# FBMFOR — Food Fraud Analysis

**MSc Food Technology and Quality Assurance | University of Reading**

[Course materials and documentation](https://ggkuhnle.github.io/fbmfor-foodfraud/)

| Practical | Launch | Method |
|-----------|--------|--------|
| Chemometrics Workbook | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ggkuhnle/fbmfor-foodfraud/blob/main/notebooks/FBMFOR_Chemometrics_Analysis.ipynb) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ggkuhnle/fbmfor-foodfraud/main?filepath=notebooks/FBMFOR_Chemometrics_Analysis.ipynb) | PCA · HCA · PLS-DA · OPLS-DA |
| XRD Starch Analysis | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ggkuhnle/fbmfor-foodfraud/blob/main/notebooks/XRD_Starch_Analysis.ipynb) | Polymorph fingerprinting · Unknown identification |

## Getting Started

1. Click a **Colab** or **Binder** badge to launch in your browser — no installation required
2. Run cells sequentially; both notebooks load demo data automatically
3. To use your own data, follow the upload instructions in Section 3 of each notebook

## Notebooks

**Chemometrics Workbook** — multivariate analysis pipeline for spectroscopic food authentication data (NMR, FTIR): PCA, HCA, PLS-DA, and OPLS-DA with preprocessing. Input: `spectra.csv` + `metadata.csv`.

**XRD Starch Analysis** — polymorph fingerprinting of starch types (Corn/A-type, Wheat/A-type, Potato/B-type, Tapioca/C-type, Unknown) in a food fraud context. Covers waterfall visualisation, peak detection and assignment, relative crystallinity estimation, and unknown sample identification. Input: `data/xrd.csv` (TwoTheta, Counts, Starch).

## Reference

Dome K, Podgorbunskikh E, Bychkov A, Lomovsky O. Changes in the Crystallinity Degree of Starch Having Different Types of Crystal Structure after Mechanical Pretreatment. *Polymers (Basel)*. 2020 Mar 12;12(3):641. [doi:10.3390/polym12030641](https://doi.org/10.3390/polym12030641). PMID: 32178224; PMCID: PMC7183072.

---

Gunter Kuhnle · Department of Food and Nutritional Sciences · g.g.kuhnle@reading.ac.uk
*For educational use within the University of Reading MSc programme.*
