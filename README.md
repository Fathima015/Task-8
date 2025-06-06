# Task 8: K-Means Clustering – Mall Customer Segmentation

## Objective
To apply K-Means clustering to segment mall customers based on their annual income, age, and spending behavior. This task demonstrates unsupervised learning and cluster evaluation techniques using Scikit-learn, Matplotlib, and Seaborn.

---

## Dataset Used
**File:** Mall_Customers.csv  
**Features available:**
- CustomerID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1-100)

---

## Key Libraries Used
- pandas
- matplotlib
- seaborn
- scikit-learn (StandardScaler, KMeans, PCA, silhouette_score)

---

## Steps Performed

### 1. Load and Inspect Dataset
- Loaded the dataset using `pandas`.
- Checked data types and verified that there were no missing values.

### 2. Visualize Dataset
- Used pairplot to analyze relationships between numerical features: Age, Income, Spending Score.
- Applied PCA to reduce these 3 features into 2 principal components and plotted them to observe natural separations.

### 3. Feature Selection and Preprocessing
- Selected **Annual Income (k$)** and **Spending Score (1-100)** as input features for clustering.
- Scaled features using `StandardScaler` to normalize the input space for KMeans.

### 4. Elbow Method to Determine Optimal Clusters
- Trained KMeans with `k` ranging from 1 to 10.
- Plotted inertia (within-cluster sum of squares) against `k`.
- Chose the optimal number of clusters (`k = 5`) based on the elbow in the plot.

### 5. KMeans Clustering
- Applied KMeans with `n_clusters=5`.
- Predicted cluster labels and added them as a new column in the dataset.

### 6. Visualize Final Clusters
- Used `seaborn.scatterplot` to visualize clusters in the original 2D space (Income vs. Spending).
- Each customer is color-coded based on their assigned cluster.

### 7. Evaluation using Silhouette Score
- Computed the silhouette score for `k = 5`.
- This score reflects how well-separated and dense the clusters are.

---

## Learning Outcomes
- Applied KMeans for customer segmentation.
- Learned to determine optimal `k` using the Elbow Method.
- Visualized high-dimensional data using PCA.
- Evaluated clustering performance using the Silhouette Score.

---
