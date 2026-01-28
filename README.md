# HCC
Spatial Fibroinflammatory Architecture Determines Immune Organization and Therapeutic Efficacy in Solid Tumors
## Spatial Fibroinflammatory Architecture Determines Immune Organization and Therapeutic Efficacy in Solid Tumors

<p align="center">
  <img src="assets/Xiaolab.jpg" alt="Xiaolab logo" width="220" />
</p>

<p align="center">
  <b>SCI manuscript companion repository</b><br />
  Analysis code, workflow figure, and supplementary materials for our study on the spatial fibroinflammatory
  architecture of solid tumors.
</p>

<p align="center">
  <b>Interactive browser:</b>
  <a href="http://8.136.123.31:8501/">in-house Xenium data</a>
</p>

---

## Table of contents
- [Overview](#overview)
- [Workflow figure](#workflow-figure)
- [Key contributions](#key-contributions)
- [Repository analysis](#repository-analysis)
- [Repository contents](#repository-contents)
- [Usage](#usage)
- [Data availability](#data-availability)
- [Project status](#project-status)
- [Citation](#citation)
- [Contact](#contact)

---

## Overview
This repository shares the analysis pipeline and figure-generation assets used in our SCI manuscript.
It aims to improve transparency and reproducibility for related tumor microenvironment studies.

## Workflow figure
<p align="center">
  <img src="assets/1.png" alt="Workflow diagram" width="820" />
</p>

## Key contributions
- **Spatial architecture**: Quantifies the organization of immune and stromal components in the tumor microenvironment.
- **Therapeutic efficacy**: Links fibroinflammatory patterns to treatment response and clinical outcomes.
- **Reproducibility**: Provides a clear, shareable workflow and supporting assets.

## Repository analysis
This repository is intentionally lightweight and focused on the analysis narrative. The notebooks follow a
single pipeline that starts with integrated scRNA-seq processing and ends with sample-level pattern discovery:

- The `code/` directory contains four Jupyter notebooks that form a sequential analysis pipeline:
  1. `_01.scRNAseq_Integration_majortype.ipynb` performs batch integration, annotates major cell types, and
     exports harmonized single-cell profiles for downstream analysis.
  2. `_02.scRNAseq_subtype.ipynb` drills into fibroblast subclusters, annotates functional programs, and
     scores gene programs (including AUCell-based signatures) to refine subtype-level signals.
  3. `_03.run_pySCENIC_scFEA.ipynb` infers regulons with pySCENIC and estimates metabolic flux with scFEA
     to connect transcriptional regulation to functional metabolism.
  4. `_04.run_NMF.ipynb` applies non-negative matrix factorization to group samples and surface latent
     patterns for interpretation and reporting.
- The `1.png` workflow figure summarizes the full pipeline at a high level.
- The `Xiaolab.jpg` image is used for branding in this README.

Overall, the repository serves as a companion to the manuscript: it documents the analysis logic and supplies
the figures needed to communicate the workflow in the paper.

## Repository contents
| Path | Description |
| --- | --- |
| `assets/` | Static images and figures used in the README. |
| `code/` | Jupyter notebooks for single-cell integration, subtype analysis, pySCENIC/scFEA, and NMF. |
| `README.md` | Project overview and guidance. |

## Usage
1. Review the workflow figure for a high-level overview.
2. Open the notebooks in order (`_01` → `_04`) to follow the analysis sequence.
3. Each notebook is designed to be self-contained with narrative notes and code cells.

## Data availability
Data files are not included in this repository. Please refer to the manuscript or supplementary materials for
details on data sources and access requirements.

## Project status
This repository is provided as a snapshot of the analysis workflow used in the study. Updates will be
announced alongside future releases or manuscript revisions.

## Citation
If you use this repository in your work, please cite the associated manuscript:

> Spatial Fibroinflammatory Architecture Determines Immune Organization and Therapeutic Efficacy in Solid Tumors.

## Contact
For questions or collaborations, please reach out to the Xiaolab team.
