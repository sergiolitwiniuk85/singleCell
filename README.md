# Single-Cell RNA Sequencing Analysis with Scanpy

![Scanpy Workflow](https://scanpy.readthedocs.io/en/stable/_images/scanpy_flowchart.png)

## Overview
This repository contains a Jupyter notebook for analyzing single-cell RNA sequencing data using the Scanpy library. The workflow demonstrates the full pipeline from data loading and preprocessing to clustering and visualization using the `paul15` hematopoietic stem cell differentiation dataset.

## Key Features
- Data preprocessing and quality control
- Normalization and feature selection
- Dimensionality reduction using PCA
- Clustering with Leiden algorithm
- UMAP visualization of cell clusters
- Comparison with original cell type annotations

## Dependencies
```bash
pip install scanpy anndata igraph leidenalg
pip install matplotlib pandas numpy seaborn
```

## Usage
1. Run the Jupyter notebook `singlecell_scanpy_paul15.ipynb`
2. The workflow includes:
   - Data loading (`sc.datasets.paul15()`)
   - Quality control (mitochondrial gene filtering)
   - Normalization and log transformation
   - Highly variable gene selection
   - PCA dimensionality reduction
   - Neighborhood graph construction
   - Leiden clustering
   - UMAP visualization

## Results
The notebook generates UMAP visualizations showing:
1. Cells colored by Leiden clustering results
2. Cells colored by original `paul15_clusters` annotations

These visualizations help identify cell populations and validate clustering against known cell types.

## Dataset
The `paul15` dataset contains:
- 2670 cells
- 18 annotated cell types
- Mouse hematopoietic stem cell differentiation data

## References
- Scanpy: [Official Documentation](https://scanpy.readthedocs.io/)
- Paul et al. (2015) Cell Stem Cell 16, 71-87
- Leiden Algorithm: [Traag et al. (2019)](https://www.nature.com/articles/s41598-019-41695-z)
