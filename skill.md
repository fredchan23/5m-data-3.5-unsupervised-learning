# Skills Demonstrated

## Assignment: Unsupervised Learning on Iris Dataset

### Skill 1: K-Means Clustering

| Item | Description |
|---|---|
| **Concept** | Partition-based clustering that groups data into K clusters by minimizing within-cluster variance (inertia) |
| **Key Technique** | Elbow Method — plot inertia vs. K and look for the "bend" where adding more clusters yields diminishing returns |
| **Evaluation** | Silhouette Score — measures how similar a point is to its own cluster vs. the nearest neighboring cluster (range: -1 to 1, higher is better) |
| **sklearn API** | `KMeans(n_clusters=k, n_init=10, random_state=42)` |
| **When to use** | Data has roughly spherical, evenly-sized clusters; number of clusters is known or discoverable via elbow/silhouette |

### Skill 2: DBSCAN Clustering

| Item | Description |
|---|---|
| **Concept** | Density-based clustering that groups together points in high-density regions and marks low-density points as noise |
| **Key Parameters** | `eps` — maximum distance between two points to be considered neighbors; `min_samples` — minimum points required to form a dense region (core point) |
| **Evaluation** | Silhouette Score + number of noise points; grid search over `eps` and `min_samples` to find the best configuration |
| **sklearn API** | `DBSCAN(eps=0.5, min_samples=5)` |
| **When to use** | Clusters have irregular shapes, varying densities, or the dataset contains noise/outliers |

### Skill 3: Data Preprocessing

| Item | Description |
|---|---|
| **Concept** | Feature standardization using `StandardScaler` to ensure all features contribute equally to distance-based algorithms |
| **Why it matters** | K-Means and DBSCAN rely on distance metrics; unscaled features with larger ranges would dominate the distance calculation |
| **sklearn API** | `StandardScaler().fit_transform(X)` |

### Skill 4: Model Comparison and Visualization

| Item | Description |
|---|---|
| **Concept** | Side-by-side comparison of clustering results against true labels to evaluate algorithm effectiveness |
| **Techniques used** | Scatter plots with color-coded clusters, centroid visualization, noise point highlighting |
| **Library** | `matplotlib.pyplot` for all visualizations |
