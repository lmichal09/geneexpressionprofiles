# Gene Expression Clustering for Cancer Subtyping

A Python-based framework to analyze, visualize, and cluster gene expression datasets to identify cancer subtypes. The project compares three clustering algorithms—**K-Means**, **Hierarchical Clustering**, and **Leiden Clustering**—applied to high-dimensional transcriptomic data, using dimensionality reduction techniques like **PCA**, **UMAP**, and **t-SNE**.

---

## 📌 Project Goal

To evaluate the effectiveness of different clustering techniques in identifying biologically meaningful cancer subtypes using gene expression data, with emphasis on:

* **Accuracy** (using ARI & Jaccard Index)
* **Stability & Coherence**
* **Scalability on large datasets**

---

## 📊 Datasets Used

* **Gene Expression Cancer RNA-Seq dataset**
* **Arcene dataset** (UCI Machine Learning Repository)

Preprocessing steps include normalization, imputation of missing values, and filtering of low-variance genes.

---

## 🔧 Methodology

### 1. **Preprocessing**

* Normalization of expression values
* Log transformation
* Imputation via `SimpleImputer`
* Low-variance gene filtering

### 2. **Dimensionality Reduction**

* **PCA** (scikit-learn)
* **UMAP** (`umap-learn`)
* **t-SNE** (scikit-learn)

### 3. **Clustering Algorithms**

* **K-Means** (`scikit-learn`)
* **Hierarchical Clustering** (Agglomerative)
* **Leiden Clustering** (`leidenalg` with modularity optimization)

### 4. **Evaluation Metrics**

* **Adjusted Rand Index (ARI)**
* **Jaccard Index**
* **Silhouette Score**
* Cluster **stability and coherence**

---

## 🖥️ How to Run

### Setup

```bash
git clone https://github.com/lmichal09/geneexpressionprofiles.git
cd geneexpressionprofiles
pip install -r requirements.txt
```

### Requirements

```txt
numpy
pandas
scikit-learn
umap-learn
leidenalg
matplotlib
seaborn
```

### Execute

You can run the project interactively using:

```bash
jupyter notebook Project.ipynb
```

Or, use the provided script (if applicable):

```bash
python run_pipeline.py --input data.csv --method leiden --reduce umap
```

---

## 📁 Directory Structure

```
├── data/                # Input expression datasets
├── figures/             # Saved output plots
├── src/                 # Core analysis scripts
│   ├── preprocessing.py
│   ├── clustering.py
│   └── dimensionality.py
├── Project.ipynb        # Main analysis notebook
├── Genomics_Project_Report-2.pdf  # Final report
└── README.md
```

---

## 📈 Results Highlights

* **PCA** explained >90% variance in <50 components
* **Leiden clustering** outperformed K-Means & Hierarchical in ARI and modularity
* **Visualizations** via UMAP/t-SNE clearly showed separation of cancer subtypes
* **Arcene dataset** excluded in final figures due to limited sample size

---

## 📚 References

* Eisen et al. (1998) *Cluster analysis and display of genome-wide expression patterns*
* MacQueen (1967) *K-means methodology*
* van der Maaten & Hinton (2008) *t-SNE visualization technique*

---

## 🧑‍💻 Author

**Leila Michal**

*lmichal09* on GitHub

📅 Project submitted: April 4th, 2025
