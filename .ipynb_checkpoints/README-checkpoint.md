# Crypto Clustering Project

## Description

This project applies **K-Means clustering** and **Principal Component Analysis (PCA)** to group cryptocurrencies based on their market performance. Using **scikit-learn**, **hvPlot**, and **Pandas**, the project identifies optimal clusters of cryptocurrencies and visualizes their relationships.

## Summary

### Part 1: Data Loading and Preparation

The first step in this project involved loading cryptocurrency market data and preparing it for clustering.

#### Key Deliverables:

- Load `crypto_market_data.csv` into a **Pandas DataFrame**.
- Generate summary statistics to understand the dataset.
- Visualize the dataset to inspect distributions and trends.

### Part 2: Data Normalization

To ensure clustering accuracy, the dataset was **standardized**.

#### Key Deliverables:

- Use **StandardScaler()** from **scikit-learn** to normalize the dataset.
- Create a new DataFrame with scaled values.
- Maintain the **coin_id** as the index for reference.

### Part 3: Finding the Optimal k for K-Means Clustering

The **elbow method** was used to determine the best number of clusters (`k`).

#### Key Deliverables:

- Implement a **for loop** to calculate inertia for `k` values from **1 to 11**.
- Plot an **Elbow Curve** to visualize the optimal `k`.
- Identify and document the best `k` value based on the elbow method.

### Part 4: K-Means Clustering on Scaled Data

Once the optimal `k` was identified, cryptocurrencies were clustered.

#### Key Deliverables:

- Initialize a **K-Means** model with the best `k`.
- Fit the model to the **scaled DataFrame**.
- Predict clusters and add them as a new column.
- Create a **scatter plot** using **hvPlot**:
  - **X-axis:** `price_change_percentage_24h`
  - **Y-axis:** `price_change_percentage_7d`
  - **Color:** Cluster labels
  - **Hover Information:** `coin_id`

### Part 5: Dimensionality Reduction with PCA

To optimize clustering, **PCA** was used to reduce dimensionality while retaining most of the dataset’s variance.

#### Key Deliverables:

- Reduce the dataset to **three principal components**.
- Compute and document the **total explained variance**.
- Create a new **PCA-transformed DataFrame**.

### Part 6: Finding the Best k Using PCA Data

Similar to the original scaled data, the **elbow method** was used on the **PCA-transformed data**.

#### Key Deliverables:

- Compute inertia for **k values from 1 to 11**.
- Plot the **Elbow Curve**.
- Compare the optimal `k` for PCA data vs. original scaled data.

### Part 7: K-Means Clustering on PCA Data

The cryptocurrencies were clustered again using the PCA-transformed dataset.

#### Key Deliverables:

- Initialize and fit a **K-Means** model.
- Predict and store the cluster labels.
- Create a **scatter plot** using **hvPlot**:
  - **X-axis:** `PC1`
  - **Y-axis:** `PC2`
  - **Color:** Cluster labels
  - **Hover Information:** `coin_id`

### Part 8: Comparing Clustering Results

To analyze the impact of dimensionality reduction, **composite plots** were created.

#### Key Deliverables:

- Compare **Elbow Curves** for original vs. PCA-transformed data.
- Compare **Cluster Visualizations** from both datasets.
- Answer: "How does reducing features affect clustering accuracy?"

## Deployment

This project was completed in **Jupyter Notebook** and submitted as a **GitHub repository**.

## Requirements

### Tools and Libraries

- **Python**
- **Jupyter Notebook**
- **Pandas**
- **scikit-learn**
- **hvPlot**
- **Matplotlib**

## Contact Information

For questions or additional information, reach out to me at:

- **Email:** ilir.hajdari111@gmail.com
