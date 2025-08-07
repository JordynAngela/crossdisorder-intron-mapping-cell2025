This project is based on data from:

Lee, S., McAfee, J. C., Lee, J., Gomez, A., Ledford, A. T., Clarke, D., Min, H., Gerstein, M. B., Boyle, A. P., Sullivan, P. F., Beltran, A. S., & Won, H. (2025). Massively parallel reporter assay investigates shared genetic variants of eight psychiatric disorders. Cell, 188(5), 1409–1424.e21. https://doi.org/10.1016/j.cell.2024.12.017
# Disorder-Linked Intron Mapping from MPRA and CROP-seq

This project extracts intron coordinates from human genes associated with psychiatric disorders, based on data from a massively parallel reporter assay (MPRA) and CRISPR-based single-cell perturbation (CROP-seq). It uses the GRCh38 human genome annotation to identify introns in genes implicated across eight major psychiatric disorders.



## Data Sources

- **MPRA data (GEO: GSE244011)**: Regulatory activity of variants tested in human neural cells
- **CROP-seq data (GEO: GSE276947)**: Gene expression after CRISPRi perturbations in hiPSC-derived neurons
- **Human genome and annotation**: Ensembl GRCh38 (release 110)

## Files in this repository

- `extract_introns_from_gtf.py`: Python script to extract intron coordinates from the GTF file
- `Homo_sapiens.GRCh38.110.gtf`: Gene annotation file used for extracting introns
- `inferred_introns.tsv`: Output table of introns with gene ID, chromosome, strand, and coordinates
- `GSE244011_dnaMatrix.csv.gz`, `GSE244011_rnaMatrix.csv.gz`: MPRA barcode and expression data

## How to Run

1. Download the GTF file and this repo
2. Run the script:
   ```bash
   python3 extract_introns_from_gtf.py
