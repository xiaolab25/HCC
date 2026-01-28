# HCC
## Spatial Fibroinflammatory Architecture Determines Immune Organization and Therapeutic Efficacy in Solid Tumors

<p align="center">
  <img src="assets/Xiaolab.jpg" alt="Xiaolab logo" width="200" />
</p>

Companion repository for a manuscript currently under peer review.  
This repo provides the core computational notebooks and lightweight assets used to run the transcriptomic analysis workflow and generate figures. No results or processed datasets are distributed here.

---

## 🌏 Interactive Browser (In-house Xenium)

[![Open Browser](https://img.shields.io/badge/Open%20Xenium%20Browser-Click%20Here-brightgreen?style=for-the-badge)](http://47.99.127.101:8501)

---

## What’s in this repository

- `code/` — Jupyter notebooks (run in order)
  1. `_01.scRNAseq_Integration_majortype.ipynb`  
     Build a unified HCC scRNA-seq reference atlas (QC → normalization → batch integration → major lineage annotation), and export harmonized profiles for downstream steps.
  2. `_02.scRNAseq_subtype.ipynb`  
     Lineage-focused re-clustering (e.g., fibroblast programs), signature scoring / program quantification (gene-set scoring, AUCell-style scoring), and subtype-level feature summaries.
  3. `_03.run_pySCENIC_scFEA.ipynb`  
     Regulatory and functional inference from scRNA-seq (pySCENIC regulons; scFEA metabolic flux features).
  4. `_04.run_NMF.ipynb`  
     Sample-level module discovery on bulk-derived cell-state fractions (consensus NMF workflow; downstream grouping/visualization utilities).

- `assets/` — figures/images used by the README and manuscript-facing materials.

---

## Workflow covered by the notebooks

1. Integrate multiple public scRNA-seq cohorts into a single reference atlas.
2. Define/annotate major lineages and refined subtypes; quantify pathway/program activities.
3. Infer transcriptional regulatory activity (regulons) and metabolic features.
4. Use the reference to support bulk RNA-seq deconvolution and sample-level ecosystem/module modeling (NMF).

> Spatial transcriptomics (Visium), in situ transcriptomics (Xenium), neighborhood/gradient quantification, and multiplex imaging (e.g., CODEX) analyses are described in the manuscript Methods; this repo focuses on the core transcriptomic notebooks and figure-generation assets.

---

## Usage

1. Run notebooks sequentially: `_01` → `_04`.
2. Each notebook expects you to provide local paths to input matrices/metadata (data are not included).
3. External requirements (not bundled here):
   - CIBERSORTx (for bulk deconvolution)
   - pySCENIC cisTarget databases (for regulon inference)
   - R packages used in downstream steps (e.g., NMF-related tooling)

---

## Data availability

Raw/processed data are not hosted in this repository.  
Public sources used by the workflow include GEO scRNA-seq cohorts (e.g., GSE149614, GSE151530, GSE156625; plus an additional public dataset described in the manuscript) and TCGA-LIHC bulk RNA-seq. Please refer to the manuscript Methods for the complete dataset list and access details.

---

## Status

Snapshot for the current submission; structure and contents may change during peer review.

---

## Contact

Xiaolab team
