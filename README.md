# CustomerCluster
> Unsupervised customer segmentation · K-Means · Agglomerative Clustering · Python

Grouping e-commerce customers into meaningful behavioural segments to enable smarter, targeted marketing strategies.

---

## Problem Statement
Most e-commerce platforms use a one-size-fits-all marketing approach. This leads to inefficient spend, missed retention opportunities, and no understanding of who the high-value customers actually are. CustomerCluster solves this by discovering natural customer groups from historical transaction data — no labels required.

---

## Dataset
- **Source:** [Customer Personality Analysis — Kaggle](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)
- **Size:** 2240 customers, 22 attributes
- **Features:** Demographics, product spending, purchase channels, campaign response, web activity

---

## Workflow

1. **EDA & Cleaning** — handled missing income values, identified and removed outliers (age > 90, income > 600k)
2. **Feature Engineering** — derived Age, Customer Tenure, Total Spending, Total Children, simplified Education and Marital Status
3. **Encoding** — OneHotEncoder on categorical features (Education, Living_With)
4. **Scaling** — StandardScaler on all features
5. **Dimensionality Reduction** — PCA to 3 components for clustering and visualisation
6. **Optimal K** — Elbow method + Silhouette Score, both converge at **K=4**
7. **Clustering** — K-Means and Agglomerative Clustering compared, Agglomerative produced tighter clusters
8. **Analysis** — Cluster profiling and business recommendations

---

## Clusters Identified

| Cluster | Label | Income | Spending | Key Trait |
|---------|-------|--------|----------|-----------|
| 0 | Family Shoppers | Low–Moderate | Low–Moderate | Deal-seeking, more children |
| 1 | Premium Loyalists | High | High | High spend, catalog & store buyers |
| 2 | Passive Segment | Low | Low | Low engagement, low spend |
| 3 | High-Value Singles | Moderate–High | High | Best campaign response, lives alone |

---

## Tech Stack
- Python, Pandas, NumPy
- Scikit-learn (KMeans, AgglomerativeClustering, PCA, StandardScaler, OneHotEncoder)
- Matplotlib, Seaborn
- Kneed (elbow detection)

---

## Key Findings
- Income and Total Spending are the strongest separating features (correlation: 0.79)
- High-income customers prefer catalog and in-store channels over web browsing
- High web visits is an inverse signal — typically indicates low-value, deal-seeking behaviour
- Cluster 3 (High-Value Singles) delivers the best ROI for marketing campaigns

---

*Minor project — BCA 6th Semester | Unsupervised Machine Learning*
