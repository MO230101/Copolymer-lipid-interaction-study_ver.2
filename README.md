# Language-Driven Exploration of Soft Polymer Interphases Using Multiscale NMR Representations

This repository contains the analysis scripts, machine learning workflows, and figure-generation pipelines used in the study:

> "Language-Driven Exploration of Soft Polymer Interphases Using Multiscale NMR Representations"

The workflows integrate:
- Time-domain NMR (TD-NMR)
- Inverse Laplace Transform (ILT) analysis
- ROI-resolved solution NMR analysis
- Meso-structure descriptor construction
- Language representation generation
- Concept-preserving preprocessing
- Bayesian Optimization (BO)
- BLOX-based novelty exploration

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
    Concept-preserving preprocessing
    BO/BLOX exploration
    Occupied fraction analysis
    Token attribution analysis

/data/
    Example datasets

/source_data/
    Source data corresponding to manuscript figures

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

# Language Representation Workflow

The language-representation workflow consists of sequential preprocessing and exploration stages:

```text
ROI-resolved NMR features
        ↓
Copolymer_change_based_motif_scores.csv
        ↓
Copolymer_MI_caption_features.csv
        ↓
Copolymer_Captions_optimized_Nplus_labels_MI_features_fixed.csv
        ↓
captions_long_preprocessed.csv
        ↓
numeric_matrix.csv
WordToken_features_concept_only.csv
        ↓
BO/BLOX exploration analysis
        ↓
Occupied fraction analysis
JSD diversity analysis
Token attribution analysis
```

Description of each stage:

```text
1. Meso-structure and interaction feature generation
   - ROI-derived motif and interaction descriptors
   - Interaction profile reconstruction

2. Caption master generation
   - Construction of N/N+SCMIDP language representations
   - Wide-format caption master table generation

3. Long-format preprocessing
   - Conversion into copolymer × variant rows
   - Tokenization-ready formatting

4. Concept-preserving preprocessing
   - Separation of numerical and concept-based representations
   - Removal of explicit numerical leakage
   - Token feature generation

5. BO/BLOX exploration analysis
   - Hybrid numerical/language representation construction
   - Exploration-space analysis
   - Occupied fraction evaluation
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
Fig5_motif_interaction_generation.ipynb
Fig5_language_representation_generation.ipynb
Fig5_longformat_preprocessing.ipynb
Fig5_concept_preprocessing.ipynb
Fig5_BO_BLOX_exploration.ipynb
```

Intermediate outputs:

```text
Copolymer_change_based_motif_scores.csv
Copolymer_MI_caption_features.csv
Copolymer_Captions_optimized_Nplus_labels_MI_features_fixed.csv
captions_long_preprocessed.csv
numeric_matrix.csv
WordToken_features_concept_only.csv
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
- PCA-based dimensionality reduction
- Hybrid numerical-language representations

Scikit-learn implementations were used unless otherwise noted.

---

# Computational Resources

Typical analyses were performed using:
- Google Colab CPU runtime
- Intel Xeon-class CPUs
- Standard RAM environments

Typical execution times:
- TD-NMR preprocessing: several minutes
- ILT analysis: several minutes
- BO/BLOX exploration: <10 min per run

No GPU acceleration was required.

---

# Data Availability

Source data underlying the manuscript figures and supplementary figures are provided in the `/source_data/` directory or with the published article.

---

# Code Availability

All custom scripts used for:
- TD-NMR preprocessing
- ILT analysis
- ROI-resolved NMR analysis
- meso-structure descriptor construction
- language representation generation
- concept-preserving preprocessing
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

Corresponding author: Jun Kikuchi

Repository maintainer: Masayuki Okada
