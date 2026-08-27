# KPP single-cell analysis code

This repository contains the analysis notebooks, intermediate results, and
figure files associated with the manuscript on the peripheral immune landscape
of *Klebsiella pneumoniae* pneumonia (KPP).

## Repository structure

The analysis is organized by main figure. Each directory contains one Jupyter
notebook together with the tables and plots generated or used by that analysis.

- `Fig 1/Figure_1.ipynb`: quality control, data integration, cell clustering and
  annotation, UMAP visualization, and immune-cell composition analyses.
- `Fig 2/Figure_2.ipynb`: inflammatory and cytokine signature scoring and
  cell-cell interaction analysis with CellPhoneDB.
- `Fig 3/Figure_3.ipynb`: CD4 T-cell subclustering and functional analyses,
  including proliferating T cells, Th1 cells, regulatory T cells, trajectory
  analysis, differential expression, and pathway enrichment.
- `Fig 4/Figure_4.ipynb`: CD8 T-cell analyses, including cytotoxicity,
  exhaustion, cell-death signatures, differential expression, and GSEA.
- `Fig 5/Figure_5.ipynb`: B-cell and plasma-cell analyses, including subtype
  composition, pseudotime, immunoglobulin expression, transcription-factor
  expression, differential expression, and functional enrichment.
- `Fig 6/Figure_6.ipynb`: myeloid-cell analyses, including monocytes, dendritic
  cells, and myeloid-derived suppressor cells; gene-regulatory-network analysis;
  and correlations between myeloid and T-cell signatures.

The `.csv`, `.txt`, `.xlsx`, and `.rnk` files in each figure directory contain
intermediate or summary results. The `.pdf` files are figure panels exported by
the corresponding notebook.

## Data availability

Newly generated sequencing data are deposited in OMIX under accession
`OMIX014353`. Public datasets and accession numbers are described in the
manuscript and Supplementary Table S1.

Raw sequencing data, processed AnnData objects, and identifiable clinical
information are not included in this repository. Some analyses therefore
require users to obtain the source data and update the input paths before
running the notebooks.

## Software requirements

The notebooks were developed in Python and use packages including:

- Scanpy, AnnData, pandas, NumPy, SciPy, and statsmodels
- Matplotlib and seaborn
- Scrublet and HarmonyPy
- CellPhoneDB and ktplotspy
- Palantir
- GSEApy
- pySCENIC, Arboreto, ctxcore, and Dask

Additional packages are imported in individual notebooks. Package versions and
computing requirements may differ between analyses, particularly for
CellPhoneDB and pySCENIC.

## Usage

1. Obtain the required source datasets described in the manuscript.
2. Install the packages imported by the notebook of interest.
3. Update all input and output paths to match the local computing environment.
4. Run the relevant notebook in its figure directory.

The notebooks are organized as analysis records and may contain steps that rely
on previously generated intermediate objects. The included result tables and
PDF files allow the principal analysis outputs to be inspected without rerunning
every computational step.
