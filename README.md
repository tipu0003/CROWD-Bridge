# CROWD-Bridge

CROWD-Bridge contains code, tables, figures, and trained model checkpoints for the manuscript on risk-aware, distributionally robust, ordinal learning and conformal evaluation for bridge decision support. The repository supports end-to-end reproducibility, including regeneration of plots and tables used in the paper.

## What this repository includes

The repository contains (i) trained model checkpoint files (`.pt`) stored via Git LFS, (ii) result spreadsheets (for example, `step7_metrics.xlsx`), and (iii) plotting scripts that export publication-ready EPS figures (for example, `figS1_paired_state_AUC_MAE.eps` and `figS2_raincloud_state_deltas.eps`).

## Repository layout

A typical layout follows this structure (names may vary by version):

- `models/`  
  Stores best checkpoints such as `A_DRO_best.pt`, `A_noDRO_best.pt`, `B_DRO_best.pt`, `B_noDRO_best.pt`.
- `figures/`  
  Stores exported figures (EPS/PDF/PNG), including supplementary figures.
- `tables/`  
  Stores LaTeX tables (`.tex`) or exported CSV/Excel tables used in the manuscript.
- `scripts/` or root-level scripts  
  Stores MATLAB/Python scripts for analysis and plotting (for example, `step7_stat_significance_plots_FIXED.m`).
- `data/` (optional, depending on licensing)  
  Stores raw/processed datasets or lightweight derived artifacts.

## Requirements

This project commonly uses:

- Git + Git LFS (required for `.pt` files)
- MATLAB (for EPS plotting scripts, if MATLAB scripts exist in the repo)
- Python (optional, if Python preprocessing/training scripts exist)
- LaTeX (optional, for manuscript compilation)

## Clone and download large files (Git LFS)

This repository tracks model checkpoints using Git LFS. Use the commands below to ensure that Git downloads the `.pt` files correctly.

```bash
git lfs install
git clone https://github.com/tipu0003/CROWD-Bridge.git
cd CROWD-Bridge
git lfs pull
