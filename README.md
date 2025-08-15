# BioInfo-ALS: Transcriptomic Analysis for ALS

## Project Overview
This project is part of a bioinformatics study focusing on transcriptomic data from patients affected by **Amyotrophic Lateral Sclerosis (ALS)**.  
The goal is to implement a **complete analysis pipeline** — from data preprocessing to identifying the most relevant genes.

---

## Analysis Steps

### **Data Preprocessing**
- Load raw transcriptomic data.
- Clean, filter, and normalize.
- Prepare gene expression tables.

### **Descriptive Analysis**
- Compute sample and gene statistics.
- Initial visualizations (distribution plots, heatmaps, etc.).

### **Dimensionality Reduction (PCA)**
- Apply **Principal Component Analysis**.
- Visualize explained variance and projections.

### **Non-linear Dimensionality Reduction**
- Apply **t-SNE** and **UMAP** for cluster visualization.

### **Univariate Analysis**
- Perform statistical tests for each gene between groups.
- Identify differentially expressed genes.

### **Multivariate Analysis – Elastic-Net (Option 1)**
- Train an **Elastic-Net Regression** model.
- Select the most informative genes based on model coefficients.

### **Multivariate Analysis – XGBoost (Option 2)**
- Train an **XGBoost Classifier**.
- Rank genes based on feature importance scores.

### **Top 100 Genes Extraction**
- Merge Elastic-Net and XGBoost results.
- Generate the final **Top 100 most relevant genes** list.

---

## Generated Results
The following CSV files are generated during the analysis:
- `upregulated_genes.csv` → Over-expressed genes  
- `downregulated_genes.csv` → Under-expressed genes  
- `significant_genes_DeSeq.csv` → Significant genes (univariate analysis)  
- `top_genes_elasticNet.csv` → Genes selected by Elastic-Net  
- `top_genes_xgboost.csv` → Genes selected by XGBoost  
- `top_100_genes.csv` → Final Top 100 gene list  
- `gene_statistics.csv` → Descriptive statistics for genes  
- `sample_statistics.csv` → Descriptive statistics for samples  

---

## Installation
```bash
# Clone the repository
git clone https://github.com/firdaouseloua/BioInfo-ALS.git
cd BioInfo-ALS

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

