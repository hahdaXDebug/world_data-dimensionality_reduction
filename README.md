# Dimensionality Reduction using Principal Component Analysis, t-SNE, and UMAP for Global Country and Information Data

**Author:** John Adrian T. Ada  
**Dataset:** Global Country Information Dataset 2023  
**Dataset DOI:** `10.34740`

## Overview
This project explores the **Global Country Information Dataset 2023** by applying various dimensionality reduction techniques. Specifically, it utilizes Principal Component Analysis (PCA), t-Distributed Stochastic Neighbor Embedding (t-SNE), and Uniform Manifold Approximation and Projection (UMAP) to visualize and analyze complex global development indicators.

The goal is to reduce the high-dimensional data into meaningful components to uncover patterns, such as identifying which countries are in need of specific types of aid (e.g., financial assistance for medical care, nutrition, health, or urban planning and infrastructure).

## Project Structure
* **Part 1 - Data Preparation**
    * **1.1 Data Loading and Cleaning:** Processing the dataset, resolving data types (e.g., converting object types to numerical), and preparing features for dimensionality reduction.
* **Part 2 - Dimensionality Reduction & Analysis** *(Extracted from notebook)*
    * Applying PCA, t-SNE, and UMAP.
    * Visualizing clustering and low-dimensional representations of the dataset.

## Key Findings & Conclusions
Based on the dimensionality reduction analysis:
* **PCA Interpretability:** PCA results are highly explainable to non-technical stakeholders. It allows us to derive new actionable features, such as creating a *Healthcare Index score* derived directly from Principal Component 1 (PC1).
* **PCA Limitations:** PCA assumes linear relationships, which struggles with non-linear features like GDP. It is also highly sensitive to outliers (e.g., Singapore).
* **UMAP Performance:** UMAP (using `n_neighbors=15` and `min_dist=0.1`) excels at visually separating the extremes of development levels (Low vs. High development level countries).
* **t-SNE Utility:** t-SNE may be useful for general exploratory data analysis and local structure visualization.

## Requirements & Dependencies
To run this notebook, you will need a Python 3 environment with the following libraries installed:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn`
* `umap-learn`

**Installation Note:** If UMAP is not available in your environment, you can install it using:
```bash
pip install umap-learn
