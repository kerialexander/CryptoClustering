# CryptoClustering - Challenge 11

## Overview
This project applies the K-means clustering algorithm and Principal Component Analysis (PCA) to classify cryptocurrencies based on their price fluctuations across multiple timeframes. The analysis focuses on price changes over 24 hours, 7 days, 30 days, 60 days, 200 days, and 1 year. By leveraging clustering techniques and dimensionality reduction, patterns in cryptocurrency price movements are identified and optimized for enhanced interpretation.

## Coding Environment
- **Language**: Python 3
- **Libraries Used**:
  - Pandas
  - NumPy
  - Scikit-learn
  - Matplotlib
  - Seaborn

## Methods and Implementation

### Data Preparation
- The dataset is loaded into a Pandas DataFrame.
- `coin_id` is set as the index.
- Data is normalized using `StandardScaler()` from scikit-learn.

### Clustering with K-Means
- The **elbow method** is used to determine the optimal number of clusters (`k`).
- The K-means model is initialized and fitted using the scaled data.
- Cluster predictions are assigned to each cryptocurrency.
- A scatter plot is generated to visualize the clusters based on selected features.

### Principal Component Analysis (PCA)
- PCA is applied to reduce the dataset to three principal components.
- The total explained variance is calculated to assess the contribution of each component.
- A new DataFrame is created with the transformed data.

### Clustering with PCA Data
- The elbow method is repeated on the PCA-transformed data to determine the optimal `k`.
- K-means clustering is applied again using the PCA data.
- A scatter plot is created to visualize the clusters in the reduced feature space.

### Feature Influence Analysis
- The weights of each feature on the principal components are analyzed.
- Strongest positive and negative influences are identified to understand the impact of different price change intervals.

## Results
- The optimal `k` for clustering is determined as **4**, consistent across both original and PCA-transformed data.
- PCA successfully reduces dimensionality while preserving **89.49%** of the variance.
- The analysis highlights short-term and long-term price movements as key differentiators in clustering outcomes.

## Questions and Answers

### What is the best value for `k`?
**Answer:** The best value for `k` is **4**.

### What is the total explained variance of the three principal components?
**Answer:** The total explained variance of the three principal components is **89.49%**.

### What is the best value for `k` when using the PCA data?
**Answer:** The best value for `k` when using the PCA data is **4**.

### Does it differ from the best k-value found using the original data?
**Answer:** No, the optimal `k` value remains **4** in both cases.

## Repository Structure
CryptoClustering/ │-- crypto_market_data.csv │-- Crypto_Clustering.ipynb │-- README.md

## Technologies Used
- **Machine Learning**: K-means clustering, PCA
- **Data Visualization**: Scatter plots, elbow curve analysis
- **Data Processing**: Feature scaling, variance analysis


