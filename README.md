## Table of Contents

- [Overview](#overview)
- [File Descriptions](#file-descriptions)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Data Requirements](#data-requirements)
- [Usage Instructions](#usage-instructions)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This repository provides tools for:

1. **cis-eQTL Analysis**: Identifying cis-regulatory genetic variants associated with gene expression for protein-coding genes.
2. **PRS Computation**: Calculating individual-level polygenic risk scores using GWAS data.
3. **GWAS Clumping and Merging**: Performing data preprocessing, including SNP clumping and merging, for further analysis.

---

## File Descriptions

1. **`cis_eqtl protein coding.ipynb`**: Notebook for conducting cis-eQTL analysis on protein-coding genes. Steps include loading gene annotations, filtering genes, and performing statistical analysis.
2. **`PRS.ipynb`**: Notebook for computing PRS for specific chromosomes. Contains scripts for working with genotype data and statistical models.
3. **`PRS_GWAS.ipynb`**: Notebook for handling GWAS preprocessing tasks, including merging and clumping variants using PLINK.

---

## Prerequisites

- Python 3.7+ installed
- Required Python packages (listed in `requirements.txt`)
- PLINK software for GWAS-related computations

---

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/y00628/dsc180a-q1-proj
   cd dsc180a-q1-proj
   ```

2. Set up a Python virtual environment:

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Ensure PLINK is installed and added to your PATH.

---

## Data Requirements

- **Gene Annotations**: Files such as `gene_annot.txt.gz` and gene expression data in `GD462.GeneQuantRPKM.50FN.samplename.resk10.txt.gz`.
- **Genotype Data**: PLINK files (.bed, .bim, .fam) for reference populations (e.g., 1000 Genomes Project).
- **GWAS Summary Statistics**: Files like `Height.gwas.txt.gz` for clumping and PRS calculations.

---

## Usage Instructions

### 1. cis-eQTL Analysis

Run the notebook `cis_eqtl protein coding.ipynb` to identify genetic variants associated with gene expression for protein-coding genes.

### 2. PRS Calculation

Run the `PRS.ipynb` notebook:

- Modify the input genotype data paths as needed.
- Use the provided Python scripts to calculate PRS for specific traits.

### 3. GWAS Preprocessing

Use `PRS_GWAS.ipynb` for SNP clumping and merging tasks:

- Ensure PLINK is properly configured.
- Update file paths and parameters in the notebook.

---

## Contributing

Contributions are welcome! Follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.
