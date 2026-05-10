# Language-Driven Exploration of Soft Polymer Interphases Using Multiscale NMR Representations

This repository contains the analysis scripts, machine learning workflows, and figure-generation pipelines used in the study:

> "Language-Driven Exploration of Soft Polymer Interphases Using Multiscale NMR Representations"

The workflows integrate:
- Time-domain NMR (TD-NMR)
- Inverse Laplace Transform (ILT) analysis
- ROI-based solution NMR analysis
- Language representation construction
- Bayesian Optimization (BO)
- BLOX-based novelty exploration
- Meso-structure descriptor generation

---

# Repository Structure

```text
/Figure1/
    Conceptual framework generation

/Figure2/
    Experimental workflow visualization

/Figure3/
    TD-NMR preprocessing
    ILT analysis
    Relaxation curve visualization
    Dynamic descriptor extraction

/Figure4/
    1D 13C NMR analysis
    HSQC analysis
    ROI processing
    Meso-structure representation

/Figure5/
    Language representation generation
    BO/BLOX exploration
    Occupied fraction analysis
    Token attribution analysis

/data/
    Example datasets

/source_data/
    Source data used for manuscript figures

/supplementary/
    Supplementary figure generation scripts
```

---

# Environment

All analyses were performed using:

- Python 3.11
- Google Colab environments
- Standard CPU-based computation

---

# Required Packages

Install required packages using:

```bash
pip install -r requirements.txt
```

Main dependencies:

```text
numpy
pandas
scipy
matplotlib
scikit-learn
sentencepiece
nmrglue
python-pptx
openpyxl
```

---

# Input Data

Representative datasets include:

```text
Addwater_CPMG_T2_Relative_Intensity.csv
AddD2O_MSE_T2_Relative_Intensity.csv
ilt_summary_ridge.csv
ilt_distributions_ridge.csv
roi_peak_features_with_blank_relative.csv
Copolymer_ROI_motif_scores.csv
captions_long_preprocessed.csv
```

---

# Figure-to-Code Mapping

## Figure 1

Conceptual illustration of language-driven polymer exploration.

Scripts:
```text
Figure1_concept_generation.ipynb
```

Outputs:
```text
Fig1.pdf
```

---

## Figure 2

Experimental and analytical workflow.

Scripts:
```text
Figure2_workflow_generation.ipynb
```

Outputs:
```text
Fig2.pdf
```

---

## Figure 3

TD-NMR relaxation analysis and ILT characterization.

Scripts:
```text
Fig3_TDNMR_ILT.ipynb
```

Input files:
```text
Addwater_CPMG_T2_Relative_Intensity.csv
AddD2O_MSE_T2_Relative_Intensity.csv
```

Outputs:
```text
Fig3a.pdf
Fig3b.pdf
Fig3c.pdf
Fig3d.pdf
```

---

## Figure 4

Solution NMR analysis and meso-structure representation.

Scripts:
```text
Fig4_solutionNMR.ipynb
```

Input files:
```text
zgpg30 spectra
HSQC spectra
ROI tables
```

Outputs:
```text
Fig4a.pdf
Fig4b.pdf
Fig4c.pdf
Fig4d.pdf
Fig4e.pdf
Fig4f.pdf
```

---

## Figure 5

Language-based exploration and occupied fraction analysis.

Scripts:
```text
Fig5_exploration.ipynb
```

Outputs:
```text
Occupied_fraction.pdf
JSD_diversity.pdf
Token_attribution.pdf
```

---

# Reproducibility

Random seeds were fixed where applicable during:
- exploration simulations
- machine learning workflows
- initialization procedures

Identical initialization conditions were used across representation types for fair comparison.

---

# Machine Learning Methods

Machine learning workflows include:

- Gaussian Process Regression (GPR)
- Bayesian Optimization (BO)
- BLOX-based novelty exploration
- PCA-based embedding analysis
- Hybrid numerical/language representations

Scikit-learn implementations were used unless otherwise noted.

---

# Computational Resources

Typical analyses were performed using:
- Google Colab CPU runtime
- Intel Xeon-class CPUs
- Standard RAM environments

Typical execution times:
- TD-NMR preprocessing: several minutes
- Exploration simulations: <10 min per run

No GPU acceleration was required.

---

# Data Availability

Source data underlying the manuscript figures and supplementary figures are provided with this repository or with the published article.

---

# Code Availability

All custom scripts used for:
- TD-NMR preprocessing
- ILT analysis
- language representation construction
- meso-structure analysis
- BO/BLOX exploration
- figure generation

are available in this repository.

---

# License

This repository is released under the MIT License.

---

# Citation

If you use this repository, please cite:

```text
Okada M., Zhu W., Amamoto Y., Kikuchi J.
Language-Driven Exploration of Soft Polymer Interphases Using Multiscale NMR Representations.
```

---

# Contact

Corresponding author:Jun kikuchi

Masayuki Okada
