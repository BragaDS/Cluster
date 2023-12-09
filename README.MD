# Credit Card Customer Clustering Analysis

## 1. Initial Visualization:
- Started with a comprehensive visualization using histograms for various columns in the DataFrame to gain insights into the data distribution.

## 2. Normality Test (Shapiro-Wilk):
- Conducted the Shapiro-Wilk normality test to assess whether the variables follow a normal distribution.

## 3. Data Standardization:
- Standardized the data using the `StandardScaler` to ensure consistent scaling across all variables.

## 4. Hopkins Test:
- Applied the Hopkins test to evaluate the clustering tendency of the dataset.

## 5. Dimensionality Reduction (PCA):
- Utilized Principal Component Analysis (PCA) to reduce the data dimensionality to two principal components.

## 6. Determining the Number of Clusters (Elbow Method):
- Employed the Elbow method to determine the optimal number of clusters.

## 7. Application of K-Means:
- Applied the K-Means algorithm for the actual clustering process.

## 8. Results Visualization:
- Visualized the clustering results using a scatter plot and a waffle chart to represent the percentage distribution of each cluster.

## 9. Detailed Cluster Analysis:
- Conducted a detailed analysis of clusters, including the count of elements in each cluster and the percentage relative to the total.

## 10. Preparation for Feature Analysis:
- Prepared the data for feature analysis by removing certain columns and applying Min-Max normalization.

## 11. Detailed Feature Visualization by Cluster:
- Plotted histograms for each feature, separated by clusters, using `FacetGrid` to delve into the nuances of feature distributions.

In summary, this analysis delves into the underlying structure of the dataset, aiming to identify groups of credit card customers with similar characteristics through clustering techniques and detailed visualizations. The multi-step process involves data exploration, statistical testing, clustering, and a thorough examination of feature distributions within clusters.
