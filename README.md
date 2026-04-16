# scrna-basics

A beginner-friendly series of Jupyter notebooks for learning single-cell RNA-seq analysis with [Scanpy](https://scanpy.readthedocs.io). Each notebook is structured as a lesson — explaining not just what to run, but what the data looks like at each step, what changed, and why it matters biologically.

## Notebooks

| # | Notebook | Topic |
|---|----------|-------|
| 0 | `scrna_cell_hashing.ipynb` | Cell hashing and sample demultiplexing: loading HTO + RNA data, CLR normalization, GMM-based singlet/doublet/negative classification, and splitting into per-sample AnnData objects |
| 1 | `scrna_basic_intro.ipynb` | End-to-end walkthrough: QC, normalization, clustering, UMAP, and cell type annotation with CellTypist |
| 2 | `scrna_batches.ipynb` | Batch effects and integration: Harmony, Scanorama, and scVI compared side-by-side; biological signal retention verified with marker genes, cluster batch composition, and CellTypist annotation |
| 3 | `scrna_differential_expression.ipynb` | Differential expression between cell types and between conditions |
| 4 | `scrna_trajectory.ipynb` | Trajectory inference and pseudotime with PAGA and Diffusion Pseudotime |

## Setup

Requires Python ≥ 3.10. Dependencies are managed with [uv](https://github.com/astral-sh/uv).

```bash
# Install uv if you don't have it
curl -LsSf https://astral.sh/uv/install.sh | sh

# Create the environment and install dependencies
uv sync --group dev

# Launch JupyterLab
uv run jupyter lab
```

## Dependencies

Core: `scanpy`, `anndata`, `numpy`, `pandas`, `matplotlib`, `scipy`  
Batch integration: `harmonypy`, `scanorama`, `scvi-tools`  
Cell typing: `celltypist`  
Clustering: `leidenalg`, `igraph`
