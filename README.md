# scRNA_CD4_Clustering 🧬

This project explores the transcriptional heterogeneity of CD4+ T lymphocytes using single-cell RNA sequencing (scRNA-seq) data.  
Our objective is to identify functional subpopulations within known types of CD4+ T cells and assign biological functions to them using clustering and enrichment analysis.

---

## 🔬 Objective

To characterize subpopulations within four known types of CD4+ T cells (Tfh, CD25^hi Tfh, Tfr, Treg) using scRNA-seq data from the human tonsils of two immunocompetent patients.

---

## 📊 Methodology Summary

- **Preprocessing & Filtering**: Gene expression matrix normalized and filtered (200 < genes/cell < 2500, mito < 15%)
- **Dimension Reduction**: PCA and UMAP
- **Trajectory Analysis**: Diffusion Pseudotime (DPT) and PAGA
- **Clustering**: Graph-based Louvain method (resolution = 2.1)
- **Differential Expression**: Kruskal-Wallis, t-test, Wilcoxon
- **Functional Enrichment**: Enrichr via gseapy on GO_Biological_Process_2021
- **Cell Type Prediction**: Random Forest classifier (accuracy = 85%)

---

## 💡 Tools & Libraries

- Python 3.10  
- `scanpy`, `anndata`, `pandas`, `seaborn`, `matplotlib`, `scikit-learn`, `gseapy`

---

## 📁 Folder Structure
scRNA_CD4_Clustering/
├── data/ # Raw input files (not included in this repo)
├── notebooks/ # Main notebook: CD4_clustering.ipynb
├── results/ # Output figures and analysis visuals
├── src/ # (Optional) Modular Python scripts
├── supplementary/ # Tables and additional materials
├── README.md
├── .gitignore
└── requirements.txt

---

## 📥 Data Access

Data from GEO (GSE214572):  
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE214572

Due to size, raw files are not included. Download and place them in the `data/` folder as described in `data/README.txt`.

---

## ✍️ Author

**Elif Maya Güngör**  
This project was conducted as part of the *Analyse de données scRNA-seq* course at Sorbonne Université.  
With contributions from: Clément Marzook Aprohim, Pape Dieng.

---

## 🌱 Status

✅ Final version — May 2025  
📊 Accuracy of ML model: 85.07%  
🧠 Ongoing personal development in machine learning & immunoinformatics

