# CD4 T Cell scRNA-seq Time Course Analysis

This project performs an integrated single-cell RNA-seq analysis of CD4 T cells at three time points (0, 12, 24 hours) following anti-CD3/CD28 stimulation, based on data from [Bibby et al. 2022](https://www.cell.com/cell-reports/fulltext/S2211-1247(22)01571-6).

## 📁 Repository Structure

- `scRNAseq_CD4_Tcell_Project.qmd`: The main analysis document.
- `data/`: Directory where raw 10X files should be placed (not included in repo).
- `images/`: Contains figures including those recreated from the paper.
- `environment.yml`: Conda environment specification.
- `README.md`: Project description and usage instructions.

## 🧪 Setup Instructions

1. **Create the Conda environment:**

```bash
conda env create -f environment.yml
conda activate scrnaseq-cd4
```

2. **Render the Quarto project:**

```bash
quarto render scRNAseq_CD4_Tcell_Project.qmd
```

## 📦 Requirements

- R >= 4.3
- Seurat
- tidyverse
- patchwork
- viridis
- harmony
- Bioconductor packages (`BiocManager`, etc.)

## 📝 Analysis Goals

- Integrate three samples of stimulated CD4 T cells.
- Annotate major CD4 T cell states.
- Recreate Figure 2B from Bibby et al.
- Perform differential gene expression across time points.

## 📊 Output

The final output is an HTML report visualizing integrated UMAPs, annotated clusters, and expression patterns of key genes.

