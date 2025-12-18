Customer Segmentation with K-Means
==================================

This project was designed to showcase skills relevant to **Data Science teams in banks and fintechs**.

- **Business perspective**: clustering results are translated into business language (risk, engagement, revenue opportunity), rather than remaining only as technical metrics.  
- **Modeling best practices**: use of normalization, justified choice of the number of clusters, and validation with appropriate clustering metrics.  
- **Clear communication**: visualizations and personas that allow non-technical areas (CRM, Risk, Product) to quickly understand the segments.  
- **Real-world applicability**: the code is organized to be easily adapted to internal card/credit datasets and integrated into analytical pipelines or CRM, risk, and marketing projects.  

## Objective

- Group customers based on their card usage behavior.  
- Evaluate the optimal number of clusters using **Inertia (WCSS)** and **Silhouette Score**.  
- Translate technical clusters into **actionable business segments**.  

## Data Source

The data was obtained from Kaggle, in the **“Credit Card Dataset for Clustering”** challenge.  
The dataset summarizes the usage behavior of about **9,000 active credit cardholders** over the last **six months**.  

## Project Pipeline

1. **Data cleaning and exploration**  
   - Handling missing values, outliers, and generating descriptive statistics.  

2. **Feature scaling**  
   - Using `StandardScaler` to standardize numerical variables.  

3. **Choosing the number of clusters (K)**  
   - Using the elbow curve (**WCSS**) and **Silhouette Score** to select K.  

4. **Model training**  
   - Applying **K-Means** and creating the `CLUSTER` column.  

5. **Cluster analysis**  
   - Calculating average statistics per cluster and creating visualizations (bar charts, radar chart).  

## Results

### Cluster 0 – High Spenders

High volume of purchases and payments, good full-payment rate, and strong potential for premium offers and credit limit increases.  

### Cluster 1 – Low Engagers

Low card usage, moderate transactional values, and focus on activation campaigns and increasing engagement.  

### Cluster 2 – Cash Advance Users

Intensive use of cash advances, lower use for purchases, and low full-payment rate, highly relevant for credit risk management and policy definition.
