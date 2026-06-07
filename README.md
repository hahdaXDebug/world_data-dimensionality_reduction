# Dimensionality Reduction using Principal Component Analysis for Global Country and Information Data

**Author:** John Adrian T. Ada  
**Dataset:** Global Country Information Dataset 2023  
**Dataset DOI:** `10.34740`

## Executive Summary
This notebook demonstrates the use of Principal Component Analysis for dimensionality reduction for the Global Country Information datset (2023) for determining foreign aid distribution. Other methods such as t-Distributed Stochastic Neighbor Embedding (t-SNE) and Uniform Manifold Approximation and Projection (UMAP) were used as exploratory tools where the ten features (Birth Rate, Fertility Rate, Infant Mortality, Life Expectancy, GDP, Unemployment Rate, Urban Population, $C0_{2}$ emmisions, Physicians per thousand and Density) were visualized by projecting them into two dimensions. Results show that two principal components were enough to explain around 70% of the data, while three components were needed to cross the 80% threshold. PC1 was defined along the x-axis of the PCA biplot and it can be generalized as the axis that refers to Health and Healthcare given the features that lie along it and the relationships present (Infant Mortality vs Life Expectancy, etc). On the other hand, PC2 can be treated as the principal component that is about Urban Development, where features such as $CO_{2}$ emissions, GDP and Urban Population are present, all being correlated with one another. UMAP, meanwhile, was preffered as a better exploratory tool for uncovering local and global structure while visualizing better intracluster compactness and cluster separation as better separates the two extremes of the development level, that being Low and High development level countries visually. 

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
