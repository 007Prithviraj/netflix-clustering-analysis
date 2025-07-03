# Netflix Movies and TV Shows Clustering

This project applies unsupervised learning techniques to cluster Netflix content based on metadata like genres, duration, and release year. The aim is to discover hidden content groupings and support personalized recommendations, content categorization, and market analysis.

---

## Dataset

- **Source**: Netflix Movies and TV Shows Metadata
- **Records**: 7,787
- **Columns**: `title`, `type`, `director`, `cast`, `country`, `release_year`, `rating`, `duration`, `listed_in`, `description`

---

## Workflow Summary

### 1. Data Cleaning & Preprocessing
- Handled missing values
- Converted duration (min/seasons) to `duration_mins`
- Derived `content_age` = current year − release year

### 2. Feature Engineering
- Extracted genres from `listed_in`
- Applied multi-label binarization to encode genres
- Scaled numerical features with `StandardScaler`

### 3. Clustering Algorithms
-  **KMeans Clustering** (with Elbow Method for `k=4`)
-  **DBSCAN** (density-based clustering)
-  **Hierarchical Clustering** (Ward linkage method)

### 4. Dimensionality Reduction & Visualization
- Applied **PCA** for 2D cluster plotting
- Created **Dendrogram** to visualize hierarchy

### 5. Cluster Interpretation

| Cluster | Interpretation |
|---------|----------------|
| 0 | International TV Shows, Crime, Drama |
| 1 | Kids’ TV, Fantasy, Animation |
| 2 | Classic Comedy, Action, Global Cinema |
| 3 | Documentaries, Popular Dramas, Global Hits |

---

## 📏 Evaluation Metrics

| Algorithm    | Silhouette Score | Davies-Bouldin Index |
|--------------|------------------|-----------------------|
| KMeans       | ~0.065           | ~3.39                 |
| DBSCAN       | ~0.0716          | ~3.29                 |
| Hierarchical | ~0.0749          | ~3.12                 |

---

## Project Files

| File | Description |
|------|-------------|
| `Netflix_Clustering_Completed.ipynb` | Full end-to-end Colab notebook |
| `netflix_clustered.csv`             | Final dataset with all cluster labels |
| `README.md`                         | Project overview and guide |

---

## Tech Stack

- Python, Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- PCA, KMeans, DBSCAN, Hierarchical Clustering

---

## Author

**Prithviraj Dwivedy**  
Data Science • ML • Python Enthusiast

---

## License

This project is for educational and portfolio use only.
