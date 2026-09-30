# GSE20592 miRNA Differential Expression Analysis

## Overview

This project analyzes miRNA expression data from the GEO dataset GSE20592.

The goal is to compare miRNA expression between normal and tumor samples and identify miRNAs with differences in expression.

## Dataset

- GEO accession: GSE20592
- 29 normal samples
- 29 tumor samples
- 720 miRNAs analyzed

The processed dataset was downloaded from the NCBI Gene Expression Omnibus (GEO).

## Analysis

The Python script performs the following steps:

1. Loads the GSE20592 dataset
2. Separates normal and tumor samples
3. Calculates average miRNA expression
4. Calculates log2 fold change
5. Performs paired t-tests
6. Applies Benjamini-Hochberg FDR correction
7. Identifies statistically significant miRNAs
8. Saves the results as a CSV file

## Significance Criteria

A miRNA was considered significant if:

- FDR < 0.05
- Absolute log2 fold change >= 1

An absolute log2 fold change of 1 represents approximately a 2-fold difference in expression.

## Results

A total of 720 miRNAs were analyzed.

Using the criteria above, **0 miRNAs met both significance criteria**.

The complete results are available in:

`GSE20592_miRNA_results.csv`

## Tools

- Python
- Pandas
- NumPy
- SciPy
- Statsmodels

## Files

```text
GSE20592-miRNA-Analysis/
├── README.md
├── mirna_differential_expression.py
└── GSE20592_miRNA_results.csv
