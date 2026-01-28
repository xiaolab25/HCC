# HCC Spatial Tumor Ecosystems
## Spatial Fibroinflammatory Architecture Determines Immune Organization and Therapeutic Efficacy in Solid Tumors

<p align="center">
  <img src="assets/Xiaolab.jpg" alt="Xiaolab logo" width="200" />
</p>

<p align="center">
  <a href="http://47.99.127.101:8501">
</p>

Companion repository for a manuscript currently under peer review.  
This repo provides the core computational notebooks and lightweight assets used to run the transcriptomic analysis workflow and generate figures. No results or processed datasets are distributed here.

---

## Workflow overview

![Workflow overview](assets/1.png)

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
  5. `_05.Visium.ipynb`  
     Visium spatial transcriptomics processing, cell-type mapping, and spatial feature analyses.
  6. `_06.xenium.ipynb`  
     Xenium in situ transcriptomics analyses and cross-modality alignment utilities.
  7. `_07.monocle2_pseudotime.ipynb`  
     Pseudotime trajectory inference and lineage progression analysis with Monocle2.

- `assets/` — figures/images used by the README and manuscript-facing materials.

---

## Workflow covered by the notebooks

1. Integrate public HCC scRNA-seq cohorts into a unified reference atlas and annotate major lineages.
2. Perform lineage-focused re-clustering/subtype annotation and quantify gene programs/signatures.
3. Infer regulatory and metabolic features from scRNA-seq (e.g., regulons and metabolic flux-related features).
4. Support bulk RNA-seq deconvolution and sample-level ecosystem/module discovery (e.g., CIBERSORTx + consensus NMF).
5. Process Visium spatial transcriptomics, map cell states to space, and derive spatial domains/features.
6. Process Xenium in situ transcriptomics, assign cell states, and run neighborhood/gradient-based spatial analyses (with cross-modality alignment utilities where needed).
7. Reconstruct pseudotime trajectories for selected lineages (Monocle2-based workflow).

> Experimental datasets and analyses (e.g., humanized PDX perturbations, multiplex imaging such as CODEX/mIF, and live imaging) are described in the manuscript Methods; only analysis notebooks and minimal figure assets are organized here.

---

## Usage

1. Run notebooks sequentially: `_01` → `_07`.
2. Each notebook expects you to provide local paths to input matrices/metadata (data are not included).
3. External requirements (not bundled here):
   - CIBERSORTx (for bulk deconvolution)
   - pySCENIC cisTarget databases (for regulon inference)
   - R packages used in downstream steps (e.g., NMF-related tooling)

---

## Data availability

Please refer to the manuscript Methods for the complete dataset list and access details.

---

## Status

Snapshot for the current submission; structure and contents may change during peer review.


---

## Contact

Xiaolab team
