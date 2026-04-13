# FBMFOR — Food Fraud Analysis

**MSc Food Technology and Quality Assurance | University of Reading**

[Course materials and documentation](https://ggkuhnle.github.io/fbmfor-foodfraud/)

| Practical | Launch | Method |
|-----------|--------|--------|
| Chemometrics Workbook | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ggkuhnle/fbmfor-foodfraud/blob/main/notebooks/FBMFOR_Chemometrics_Analysis.ipynb) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ggkuhnle/fbmfor-foodfraud/main?filepath=notebooks/FBMFOR_Chemometrics_Analysis.ipynb) | PCA · HCA · PLS-DA · OPLS-DA |
| XRD Starch Analysis | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ggkuhnle/fbmfor-foodfraud/blob/main/notebooks/XRD_Starch_Analysis.ipynb) | Polymorph fingerprinting · Unknown identification |
| FTIR Honey Analysis | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ggkuhnle/fbmfor-foodfraud/blob/main/notebooks/FTIR_Honey_Analysis.ipynb) | Overlay/waterfall plots · Fingerprint region · PCA |
| NMR Honey Analysis | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ggkuhnle/fbmfor-foodfraud/blob/main/notebooks/NMR_Honey_Analysis.ipynb) | Bruker TopSpin · Waterfall plots · Spectral binning · PCA |
| IRMS Olive Oil Origin | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ggkuhnle/fbmfor-foodfraud/blob/main/notebooks/IRMS_Olive_Oil_Origin.ipynb) | δ²H/δ¹⁸O origin map · δ¹³C C3/C4 strip · Nearest-centroid assignment |
| SEM Food Microscopy | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ggkuhnle/fbmfor-foodfraud/blob/main/notebooks/SEM_Food_Microscopy.ipynb) | Gallery · Image statistics · CV texture comparison · Histograms |

## Getting Started

1. Click a **Colab** or **Binder** badge to launch in your browser — no installation required
2. Run cells sequentially; both notebooks load demo data automatically
3. To use your own data, follow the upload instructions in Section 3 of each notebook

## Notebooks

**Chemometrics Workbook** — multivariate analysis pipeline for spectroscopic food authentication data (NMR, FTIR): PCA, HCA, PLS-DA, and OPLS-DA with preprocessing. Input: `spectra.csv` + `metadata.csv`.

**XRD Starch Analysis** — polymorph fingerprinting of starch types (Corn/A-type, Wheat/A-type, Potato/B-type, Tapioca/C-type, Unknown) in a food fraud context. Covers waterfall visualisation, peak detection and assignment, relative crystallinity estimation, and unknown sample identification. Input: `data/xrd.csv` (TwoTheta, Counts, Starch).

**FTIR Honey Analysis** — ATR-FTIR analysis of honey samples for authentication. Reads Perkin-Elmer Spectrum CSV exports (already baseline-corrected), plots overlay and waterfall spectra with diagnostic band annotations, and runs PCA on the carbohydrate fingerprint region (1800–650 cm⁻¹). Sample IDs derived from filenames. Input: `data/ftir/*.csv`.

**NMR Honey Analysis** — ¹H NMR analysis of honey samples using Bruker TopSpin data. Reads binary `1r` processed spectra directly, displays waterfall plots of reference sugars and unknown honey samples separately, and runs PCA on binned spectral data (0.04 ppm bins, 0.5–9.0 ppm, HDO region excluded). Input: `data/nmr/` (Bruker experiment directories).

**IRMS Olive Oil Origin** — stable isotope ratio analysis for geographic origin verification and adulteration detection. Loads long-format CSV (Sample/delta/IR columns), pivots to wide, plots δ²H vs δ¹⁸O against published Mediterranean reference ellipses (Italy, Spain, Greece, Tunisia), and a δ¹³C C3/C4 adulteration strip. Nearest-centroid assignment with ambiguity flagging. Input: `data/irms/irms.csv`.

**SEM Food Microscopy** — scanning electron microscopy image analysis. Loads 16-bit greyscale TIFFs grouped by sample code, displays a contact-sheet gallery, and computes per-image statistics (mean intensity, SD, CV) as texture proxies. CV bar chart and pixel-distribution histograms compare microstructural heterogeneity across samples. Input: `data/sem/*.tif`.

## References

- Dome K et al. Changes in the Crystallinity Degree of Starch Having Different Types of Crystal Structure after Mechanical Pretreatment. *Polymers (Basel)*. 2020;12(3):641. [doi:10.3390/polym12030641](https://doi.org/10.3390/polym12030641)
- Torres-Cobos B et al. Discrimination of Italian and non-Italian virgin olive oils by stable isotope ratio analysis. *Food Chemistry*. 2025. [doi:10.1016/j.foodchem.2024.141998](https://doi.org/10.1016/j.foodchem.2024.141998)
- Bontempo L et al. Multi-element stable isotope ratio analysis for determining the geographical origin of Italian extra-virgin olive oils. *Food Control*. 2019;98:482–489. [doi:10.1016/j.foodcont.2018.11.038](https://doi.org/10.1016/j.foodcont.2018.11.038)
- Szaniawska A et al. Data-Driven FTIR Spectroscopy for the Discrimination of Nectars. *Molecules*. 2025;30(20):4083. [doi:10.3390/molecules30204083](https://doi.org/10.3390/molecules30204083)

---

Gunter Kuhnle · Department of Food and Nutritional Sciences · g.g.kuhnle@reading.ac.uk
*For educational use within the University of Reading MSc programme.*
