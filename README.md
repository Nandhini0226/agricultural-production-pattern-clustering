# 🌾 Agricultural Production Pattern Analysis Using K-Means Clustering

## 📌 Project Overview

This project applies the **K-Means Clustering** algorithm to identify agricultural production patterns among paddy farms. The clustering is performed using farm characteristics, weather conditions, soil type, and agricultural input variables to discover groups of farms with similar production patterns.

The paddy yield variable is **not used during clustering**. Instead, it is used after clustering to evaluate which farming pattern is associated with higher productivity.

---

## 🎯 Project Objectives

* Cluster paddy farms based on weather conditions, soil type, agricultural inputs, and farm characteristics.
* Identify the farming pattern associated with the highest paddy yield by comparing the average yield of each cluster.

---

# 📂 Dataset

* **Source:** Original project GitHub repository
* **Format:** CSV
* **Original Size:** 2,789 rows × 45 columns

### Dataset Summary

| Item              | Value |
| ----------------- | ----: |
| Total Records     | 2,789 |
| Total Features    |    45 |
| Missing Values    |     0 |
| Duplicate Records |   451 |
| Final Records     | 2,338 |

---

# 🧹 Data Cleaning

The following preprocessing steps were performed:

* Removed **451 duplicate records**
* Verified categorical variables for consistency
* No category standardization was required
* Converted numerical variables to **float** format

Final cleaned dataset:

* **2,338 farm records**

---

# ⚙️ Data Preprocessing

The dataset was prepared before clustering by:

* Separating the **Paddy Yield** variable
* Standardizing numerical variables using **StandardScaler**
* Encoding categorical variables using **One-Hot Encoding**
* Scaling all features before clustering

Processed dataset:

* **2,338 records**
* **71 features**

---

# 📊 Determining the Optimal Number of Clusters

Two methods were used:

* **Elbow Method**
* **Silhouette Analysis**

### Selected Number of Clusters

**K = 3**

The Elbow Method indicated three clusters as the best balance between simplicity and clustering performance.

---

# 🤖 K-Means Model

Model Parameters

```python
KMeans(
    n_clusters=3,
    random_state=42,
    n_init=10
)
```

The model assigns each farm to one of three production clusters.

---

# 📈 Cluster Distribution

| Cluster | Farms |
| ------: | ----: |
|       0 |   765 |
|       1 |   711 |
|       2 |   862 |

The clusters are relatively balanced.

---

# 🌾 Average Paddy Yield by Cluster

| Cluster | Average Yield (Kg) |
| ------: | -----------------: |
|       0 |          22,591.16 |
|       1 |          22,468.06 |
|       2 |      **22,744.11** |

**Cluster 2** achieved the highest average paddy yield.

---

# 🔍 Cluster Characteristics

## Cluster 0

* Moderate fertilizer usage
* Moderate rainfall
* Moderate humidity
* Medium productivity

---

## Cluster 1

* Higher humidity
* Lower temperatures
* Lower fertilizer application
* Lowest average yield

---

## Cluster 2

* Higher fertilizer application
* Greater pest management
* Higher late-stage temperatures
* Highest average yield

---

# 🌱 Categorical Feature Insights

### Agriblock

Clusters were strongly separated by geographical location.

* Cluster 0 → Cuddalore & Kurinjipadi
* Cluster 1 → Chinnasalem & Kallakurichi
* Cluster 2 → Sankarapuram & Panruti

---

### Soil Type

Clay soil was the dominant soil type across all clusters.

---

### Rice Variety

The most common varieties were:

* Ponmani
* Deluxe Ponni

CO_43 appeared less frequently.

---

### Nursery Type

Dry nursery was slightly more common than wet nursery in all clusters.

---

# 📌 Key Findings

* Three distinct agricultural production patterns were identified.
* Cluster 2 produced the highest average paddy yield.
* Geographical location (Agriblock) played a major role in cluster formation.
* Clay soil was the dominant soil type.
* Ponmani and Deluxe Ponni were the most commonly cultivated rice varieties.
* Dry nursery practices were slightly more prevalent.

---

# 🛠️ Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

# 📚 Machine Learning Techniques

* Data Cleaning
* Feature Engineering
* StandardScaler
* One-Hot Encoding
* Elbow Method
* Silhouette Analysis
* K-Means Clustering

---

# 🚀 Results

The K-Means algorithm successfully grouped **2,338 paddy farms** into **three meaningful production patterns** without using yield during training.

The identified clusters provide valuable insights into how environmental conditions, agricultural inputs, and geographical factors influence farming practices and productivity.

---

# ✅ Conclusion

This project demonstrates that unsupervised machine learning can effectively identify agricultural production patterns. The discovered clusters help explain differences in farming practices and productivity, making the approach useful for farmers, researchers, and agricultural planners interested in data-driven decision making.

---

## 👨‍💻 Author

**Agricultural Production Pattern Analysis Using K-Means Clustering**
