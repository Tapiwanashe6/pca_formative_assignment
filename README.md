# Malaria Dataset PCA Analysis

## Overview
This project performs **Principal Component Analysis (PCA)** on the `DatasetAfricaMalaria.csv` dataset.  
The goal is to **reduce the dimensionality** of the dataset while preserving as much variance as possible, and to visualize the data in a lower-dimensional space.

---

## Dataset
- File: `DatasetAfricaMalaria.csv`  
- Contains malaria-related numeric features for different African countries.  
- Includes a `Country Name` column and several numeric features.  
- Missing values are handled by replacing them with column means.  

---

## Steps Performed

1. **Load and Standardize Data**
   - Only numeric columns are selected.
   - Missing values are replaced with column means.
   - Standardization ensures features have mean 0 and standard deviation 1.

2. **Compute Covariance Matrix**
   - Covariance matrix of standardized data is calculated using NumPy.

3. **Eigendecomposition**
   - Eigenvalues and eigenvectors of the covariance matrix are computed.
   - Eigenvectors represent the principal components.

4. **Sort Principal Components**
   - Components are sorted by eigenvalues in descending order (largest variance first).

5. **Project Data**
   - Data is projected onto the top principal components.
   - Number of components chosen to retain ~90% of variance.

6. **Visualization**
   - Original feature space (first two features) is plotted.
   - PCA-transformed data is plotted with countries labeled (every 30th country to avoid clutter).

---

## Requirements
- Python 3.x  
- Libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`

> Note: This project uses **NumPy only for calculations** (no scikit-learn for PCA).

---

## Usage
1. Open the notebook `Malaria_PCA.ipynb` in **Google Colab** or **VS Code**.  
2. Run all cells sequentially.  
3. Visualize PCA results and analyze the dimensionality-reduced dataset.  

---

## Output
- `reduced_data`: PCA-transformed dataset.  
- Plots:
  - Original feature space (first two features)
  - PCA projection with top 2 principal components and labeled countries

---

## Author
Tapiwanashe Marufu  

