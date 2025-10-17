#  Data Files Description

## *File List*
- `expression_data.txt` - Gene expression data (GSE176078)
- `sample_metadata.csv` - Patient clinical information data

## *Data Source*
- **Research Paper**: Wu et al. 2021, Nature Genetics
- **Database**: GSE176078 (GEO Database)
- **Cancer Type**: Breast Cancer
- **Data Type**: Bulk RNA-seq gene expression data
- **Sample Size**: 30 breast cancer patient samples

## *Data Details*
### expression_data.txt
- **Format**: TSV file (tab-separated values)
- **Structure**: Genes (rows) × Patients (columns) matrix
- **Values**: Gene expression count values
- **Key Genes**: PDCD1, CD274, CD8A, IFNG and other immune-related genes
### sample_metadata.csv
- **Format**: CSV file
- **Content**: Patient ID, cell type, tumor subtype information
- **Usage**: Result interpretation

## *Usage Instructions*
```python
import pandas as pd
import numpy as np

# Load gene expression data
expression_data = pd.read_csv('data/expression_data.txt', sep='\t', index_col=0)
metadata = pd.read_csv('data/sample_metadata.csv')

# Check basic data information
print(f"Number of genes: {expression_data.shape[0]}")
print(f"Number of patients: {expression_data.shape[1]}")
print(f"Data type: {expression_data.dtypes.iloc[0]}")
