# Task 2

This repository contains the code and outputs for **Task 2** in preparation for interview for the role of **Research Assistant in Bioinformatics (155546)**.

The purpose of this project was to:
1. Identify genes whose expression changes correspond with changes in cell morphology
2. Represent the potential function of these genes relative to cell morphology.
3. Provide statistical support for the methods chosen and results obtained.

This project is based on data and analysis from the Scala et al. paper published in 2021 titled:
[Phenotypic variation of transcriptomic cell types in mouse motor cortex](https://www.nature.com/articles/s41586-020-2907-3)

The following repository is a clean and efficient application of the publicly available data to answer the above aims. 

---

## Repository Structure

```
Task2_155546/
├── README.md
├── environment.yml    # Conda environment for the Python notebooks
│
├── data/                                     # All input data sourced from berenslab/mini-atlas repository 
│   ├── m1_patchseq_meta_data.csv             # Metadata 
│   ├── m1_patchseq_morph_zprofiles.csv       # Neuron z-profiles 
│   ├── m1_patchseq_morph_features.csv        # Neuron morphological features (numerical)
│   ├── m1_patchseq_exon_counts.csv.gz        # Neuron exon count matrix
│   ├── m1_patchseq_intron_counts.csv.gz      # Neuron intron count matrix
│   └── processed/                            # Output data from code/ notebooks
│
└── code/
    ├── 01_cell_selection.ipynb               # Stage 1: cell selection, data interrogation
    ├── 02_pairwise_PC_correlation.ipynb      # Stage 2: identification of correlations between gene expression and morphology
    └── rnaseqTools.py                        # Functions for rnaseq analysis taken from berenslab/mini-atlas/code repository
```

## Environment & installation

A conda environment is provided at the base of this repository, mirroring the environment needed for all analyses. 

```bash
git clone <repo-url> Task2_155546
cd Task2_155546

conda env create -f environment.yml
```
