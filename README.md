# Crypto Clustering Project Challenge

## Before You Begin

### Repository Setup
1. Create a new repository named **CryptoClustering** on GitHub.
2. Clone the new repository to your local machine.
3. Add all project-related files to this repository.
4. Commit and push your changes to GitHub regularly.

### Files Provided
- `Crypto_Clustering.ipynb`: The Jupyter Notebook for executing the clustering analysis.
- `crypto_market_data.csv`: The dataset containing cryptocurrency market data.

## Project Overview
This project involves clustering cryptocurrencies based on their market performance using **K-Means Clustering** and **Principal Component Analysis (PCA)**. The objective is to compare clustering results before and after dimensionality reduction.

---

## Instructions

### **Step 1: Load and Explore the Data**
- Load `crypto_market_data.csv` into a **Pandas DataFrame**.
- Display summary statistics.
- Plot the data to understand trends before processing.

### **Step 2: Data Preprocessing**
- Use `StandardScaler()` from `scikit-learn` to normalize the data.
- Create a new DataFrame with the scaled values.
- Set `coin_id` as the index.

### **Step 3: Find the Best k for K-Means Clustering**
- Use the **elbow method**:
  1. Create a list of k values from **1 to 11**.
  2. Compute the **inertia** for each k.
  3. Plot the elbow curve to identify the optimal k.
  4. Answer: *What is the best value for k?*

### **Step 4: Cluster Cryptocurrencies Using K-Means**
- Initialize and fit the **K-Means model** with the best k.
- Predict clusters and add them to the DataFrame.
- **Visualization:**
  - Create a scatter plot using `hvPlot`.
  - Set x = `price_change_percentage_24h`, y = `price_change_percentage_7d`.
  - Color points by cluster labels.
  - Use `hover_cols` to show the `coin_id`.

### **Step 5: Optimize Clustering with PCA**
- Reduce the dataset to **three principal components** using PCA.
- Retrieve explained variance and answer: *What is the total explained variance?*
- Create a new DataFrame with PCA-transformed data.

### **Step 6: Find the Best k for PCA Data**
- Repeat the **elbow method** using the PCA-transformed data.
- Compare the optimal k value with the one found earlier.

### **Step 7: Cluster Cryptocurrencies Using PCA Data**
- Fit **K-Means** on the PCA DataFrame using the best k.
- Predict clusters and add them to the DataFrame.
- **Visualization:**
  - Create a scatter plot with x = `PC1`, y = `PC2`.
  - Color points by cluster labels.
  - Use `hover_cols` to show `coin_id`.
- Answer: *What is the impact of using fewer features?*

### **Step 8: Compare Clustering Results**
- Use `hvPlot` to create **composite plots**:
  - Compare the elbow curves from original and PCA-transformed data.
  - Compare clustering results before and after PCA.
  - Analyze how reducing features affected clustering.

---

## **Conclusion**
This project explores clustering analysis in the cryptocurrency market, comparing the impact of dimensionality reduction. By applying **K-Means and PCA**, we evaluate how reducing features affects clustering performance and interpretation.
