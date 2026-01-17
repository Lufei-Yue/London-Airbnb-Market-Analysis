# 🇬🇧 London Airbnb Market Analysis
### Spatial Data Science & Market Segmentation Strategy

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Libraries](https://img.shields.io/badge/Library-Pandas%20%7C%20GeoPandas%20%7C%20Scikit--Learn-green)
![Focus](https://img.shields.io/badge/Focus-Spatial%20Analysis%20%26%20Clustering-orange)

## Summary
This project utilises **spatial data science** and **unsupervised machine learning (K-Means)** to analyse the complex London short-term rental market. By processing real-world data from *Inside Airbnb*, the analysis identifies high-yield investment zones and segments the market into distinct operational personas, providing actionable insights for investors and policymakers.

## Key Business Problems Solved
1.  **Investment Strategy:** Identifying boroughs that offer the best balance between entry cost (price) and tourist demand (review volume).
2.  **Market Segmentation:** Moving beyond simple pricing to understand the distinct business models operating in London (e.g., "Occasional Sharers" vs "Commercial Hotels").

## Methodology & Tech Stack

### 1. Data Cleaning & Engineering
* **Raw Data Processing:** Handled dirty data (currency symbols, mixed types) using Regex and Pandas.
* **Outlier Removal:** Filtered extreme luxury assets (£1,000+) to focus on the mass market.
* **Standardisation:** Applied `StandardScaler` to normalise features for clustering algorithms.

### 2. Geospatial Analysis
* **Mapping:** Utilised **GeoPandas** and `contextily` to project listing data onto official London Borough boundaries (EPSG:3857).
<img width="1773" height="1589" alt="image" src="https://github.com/user-attachments/assets/25545fc2-8d31-43f2-9989-2b1247fac501" />

* **Visualisation:** Created professional choropleth maps with optimised labelling strategies for dense urban areas.
<img width="1773" height="1589" alt="image" src="https://github.com/user-attachments/assets/85430466-255b-4039-87f5-cdbf872dbd54" />


### 3. Machine Learning (Clustering)
* **Algorithm:** K-Means Clustering.
* **Optimisation:** Used the **Elbow Method** to determine the optimal cluster count ($K=5$).
<img width="1773" height="1589" alt="image" src="https://github.com/user-attachments/assets/5572c6b1-c713-41df-9c16-becec898a9a1" />

* **Interpretation:** Decoded mathematical clusters into business personas (e.g., *The Budget Kings*, *The Commercial Ops*).
![Uploading image.png…]()


## Key Insights & Visualisations

### The Investment "Sweet Spot"
While **Westminster** is the most expensive, boroughs like **Islington** and **Lambeth** showed the highest efficiency—moderate pricing with exceptional review engagement.

### Market Personas (The 5 Clusters)
The K-Means model identified five distinct operator types:
* **Cluster 0 (The Occasional Sharers):** Low availability (~88 days). Compliant with regulations.
* **Cluster 1 (The Commercial Ops):** High availability (~311 days). High regulatory risk.
* **Cluster 2 (The Budget Kings):** Low price (£103) but massive review volume. High turnover strategy.
* **Cluster 4 (The Long-Term Lets):** Extreme minimum nights (~274 days). Residential tenancies bypassing agents.



