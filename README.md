# scRNA-seq Variability Analysis: GSE139324

## 🔬 Project Title
Can variations in single-cell RNA-seq be used as predictive biomarkers for disease progression?

## 📌 Problem Statement
Studies suggest that variations in single-cell data can provide biological information rather than just noise.  
Zheng et al. (2023) showed that B cells from aged individuals vs. younger individuals display higher variability, pointing to transcriptional noise as a biomarker of aging.  
However, variability-based biomarkers remain underexplored for disease prediction and clinical decision-making.

## 🎯 Objectives
- Quantify transcriptional variability in scRNA-seq datasets across different disease or condition states.
- Compare predictive power of variability-based features vs. mean-expression features.
- Identify enriched pathways with high transcriptional variability during cellular transitions.
- Develop a reproducible computational pipeline for variability-driven biomarker discovery.

## 📂 Dataset
- **Source**: GEO accession [GSE139324](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE139324)  
- **Type**: Human PBMC scRNA-seq (10x Genomics format)  

Raw files are **not stored in this repo** due to size.  
Download from GEO and place inside `data/raw/`.

## ⚙️ Methodology
1. **Preprocessing**: filtering, normalization, HVG selection.  
2. **Dimensionality reduction**: PCA + UMAP.  
3. **Clustering**: Leiden clustering.  
4. **Annotation**: Marker-based cluster annotation.  
5. **Validation**: Dotplot, heatmap, differential gene expression.  

## 📊 Results (so far)
### Annotated cell types (GSM4138110 sample):
| Leiden Cluster | Cell Type                  | Representative Markers | Cell Count | % of Total |
|----------------|----------------------------|-------------------------|------------|------------|
| 0              | Classical Monocytes        | CD14, LYZ              | 545        | 31.7%      |
| 1              | CD8+ T cells               | CD3D, CD8A, NKG7       | 401        | 23.3%      |
| 2              | CD4+ T cells               | CD3D                   | 360        | 20.9%      |
| 3              | Activated/Prolif. T cells  | CD3D, MKI67            | 225        | 13.1%      |
| 4              | Non-classical Monocytes    | FCGR3A, LST1           | 113        | 6.6%       |
| 5              | B cells                    | MS4A1                  | 42         | 2.4%       |
| 6              | NK cells                   | NKG7                   | 35         | 2.0%       |

Figures are in `/figures/`:
- UMAP plots (clusters, markers, cell types)  
- PCA plot  
- Dotplots & heatmaps of markers  

## 📦 Installation
Clone repo:
```bash
git clone https://github.com/your-username/scRNAseq-variability.git
cd scRNAseq-variability


