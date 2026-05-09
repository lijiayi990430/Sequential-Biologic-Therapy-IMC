# Sequential Biologic Therapy IMC

This repository contains figure-generation notebooks and supporting analysis code for the manuscript:

**Spatial Immune Microenvironment Succession During Sequential Biologic Therapy: Evidence from a Patient with Refractory Ulcerative Colitis**

## Overview

This code accompanies a longitudinal imaging mass cytometry (IMC) study of the mucosal immune microenvironment in a patient with refractory ulcerative colitis undergoing sequential biologic therapy. The disease course was divided into five clinically defined periods:

- **P1**: baseline active disease
- **P2**: remission following infliximab therapy
- **P3**: secondary loss of response to infliximab
- **P4**: non-response to vedolizumab with extraintestinal manifestation
- **P5**: remission following ustekinumab treatment

The notebooks reproduce the figure panels used to analyze immune-cell composition, macrophage subset remodeling, spatial relationships between T-cell subsets and macrophages, distance-dependent enrichment patterns, and the spatial organization of the IL-1β⁺ M1–TNFα⁺ CD4⁺ T-cell axis.

This repository is intended for research transparency and reproducibility. It is not intended for clinical decision-making or diagnostic use.

## Repository contents

| Notebook | Associated figure panel | Purpose |
|---|---:|---|
| `Fig1C. Heatmap.ipynb` | Fig. 1C | Generates the single-cell annotation heatmap / immune-cell landscape summary. |
| `Fig1D. Immune cell distribution and relative abundance.ipynb` | Fig. 1D | Visualizes immune-cell distribution and relative abundance across P1–P5. |
| `Fig2A. M1_M2_Macrophage_Dynamics.ipynb` | Fig. 2A | Analyzes temporal changes in infiltrating macrophages (M1), resident macrophages (M2), and the M1/M2 ratio. |
| `Fig2C. Mean distances between T-cell subsets and macrophage subsets.ipynb` | Fig. 2C | Quantifies local enrichment and mean spatial distances between CD4⁺/CD8⁺ T cells and M1/M2 macrophages. |
| `Fig2D. M1_M2_mean_distance.ipynb` | Fig. 2D | Compares mean distances from total T cells, CD4⁺ T cells, and CD8⁺ T cells to M1 versus M2 macrophages. |
| `Fig3A. M1_radial_density_CD4_CD8_side_by_side.ipynb` | Fig. 3A | Computes and visualizes distance-stratified radial density distributions of CD4⁺ and CD8⁺ T cells around M1 macrophages. |
| `Fig3B. Stagewise_CDF_CD4_vs_CD8_to_nearest_M1.ipynb` | Fig. 3B | Compares stage-specific cumulative distribution functions (CDFs) of CD4⁺ versus CD8⁺ T-cell distances to nearest M1 macrophages. |
| `Fig3C. CDF_CD4_CD8_to_nearest_M1.ipynb` | Fig. 3C | Performs cross-stage comparison of nearest-distance profiles from CD4⁺ and CD8⁺ T cells to M1 macrophages. |
| `Fig4. IL-1β⁺ M1 and TNFα+CD4+T.ipynb` | Fig. 4 | Analyzes bidirectional spatial enrichment between IL-1β⁺ M1 macrophages and TNFα⁺ CD4⁺ T cells. |

## Data

The notebooks are designed to operate on de-identified IMC-derived single-cell and spatial-analysis tables generated from colonic mucosal biopsy sections.

Raw clinical identifiers are not included in this repository. Raw IMC data and original tissue-section images are described in the manuscript as supplementary data files:

- **Data file S1**: de-identified raw imaging mass cytometry data
- **Data file S2**: original tissue-section images

If you use this repository with your own data, place input files in a local `data/` directory or modify the file paths inside each notebook accordingly.

## Computational environment

The notebooks were developed for Python-based analysis in Jupyter Notebook / JupyterLab. A typical environment should include:

```bash
python >= 3.9
jupyterlab
numpy
pandas
scipy
matplotlib
seaborn
scikit-learn
openpyxl
```

To create a local environment:

```bash
python -m venv .venv
source .venv/bin/activate      # macOS/Linux
# .venv\Scripts\activate     # Windows

pip install --upgrade pip
pip install jupyterlab numpy pandas scipy matplotlib seaborn scikit-learn openpyxl
```

Then launch JupyterLab:

```bash
jupyter lab
```

Open and run the notebooks corresponding to the figure panels of interest.

## Reproducibility notes

1. The notebooks are organized by figure panel rather than as a single end-to-end pipeline.
2. File paths inside the notebooks may need to be adjusted depending on where input data are stored.
3. Some figure panels depend on preprocessed single-cell annotation tables, spatial-coordinate data, or distance matrices derived from IMC segmentation output.
4. The repository is intended to reproduce the analytical logic and visualization workflow used in the manuscript figures.

## Citation

If you use this code, please cite the associated manuscript and the archived software record once available.

**Manuscript citation**

> Li J, Li C, Li Z, Li H, Li H, Feng Z, Yi Q, Sun G, Zhang D, Sheng J, Cao X, Liu X. *Spatial Immune Microenvironment Succession During Sequential Biologic Therapy: Evidence from a Patient with Refractory Ulcerative Colitis*. Manuscript under review.

**Code citation**

> Sequential Biologic Therapy IMC analysis code. Zenodo DOI: `to be added after archive`.

## License

The analysis code in this repository is released under the MIT License. See the `LICENSE` file for details.

The license applies to code only. Clinical data, raw IMC data, tissue-section images, and other patient-derived materials are not covered by this software license and remain subject to the original ethics approval, patient consent, institutional policies, and journal data-availability terms.

## Contact

For questions about the study design, data access, or code implementation, please contact the corresponding authors listed in the manuscript.
