# Iris Dataset Clustering


## 📊 Dataset

The Iris dataset was obtained from the `sklearn` library.

It contains **150 observations** and **4 numerical features**:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

The dataset also contains species labels. However, since this is an **unsupervised clustering problem**, the species labels were not used during clustering.

---

## 🔧 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the Iris dataset using `sklearn`.
2. Converted the feature data into a Pandas DataFrame.
3. Checked for missing values.
4. Checked for duplicate records.
5. Performed outlier analysis using boxplots.
6. Potential outliers were observed in the Sepal Width feature, but they were retained because they are valid observations from the original dataset.
7. Standardized all four numerical features using `StandardScaler`.

Feature scaling was performed because both KMeans and Hierarchical Clustering rely on distance calculations.

---

## 🤖 Algorithms Implemented

### 1. KMeans Clustering

KMeans is an unsupervised clustering algorithm that divides data into a predefined number of clusters. It initializes cluster centroids, assigns each observation to its nearest centroid, recalculates the centroids, and repeats the process until the clusters become stable.

For this project, KMeans was applied with **3 clusters**.

#### Visualization

The resulting clusters were visualized using:

- Petal Length
- Petal Width

Although only two features are used for visualization, all four scaled features were used for clustering.

#### Evaluation

The KMeans model was evaluated using:

- Silhouette Score
- Inertia
- Elbow Method

---

### 2. Hierarchical Clustering

Hierarchical clustering is an unsupervised learning technique that creates a hierarchy of clusters. In the agglomerative approach, each observation initially forms an individual cluster, and the closest clusters are progressively merged.

A **dendrogram** was used to visualize the hierarchical structure.

The **Ward linkage method** was used to create compact clusters.

The final model was configured to produce **3 clusters**.

#### Visualization

The resulting clusters were visualized using:

- Petal Length
- Petal Width

A dendrogram was also created to visualize the merging process.


## 📈 Results

Both KMeans and Hierarchical Clustering were able to identify three distinct groups within the Iris dataset.

The visualizations show that one group is clearly separated, while some overlap exists between the other two groups. This is expected because some Iris observations have similar feature characteristics.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- SciPy
- Jupyter Notebook

---

## 📁 Project Structure

```text
Iris-Clustering/
│
├── Iris_Clustering.ipynb
└── README.md
