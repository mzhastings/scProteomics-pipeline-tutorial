# Differential Expression with limpa

## Installation
- Download [limpa](https://www.bioconductor.org/packages/release/bioc/html/limpa.html)

## Usage
Expression matrix (expr), gene table (genes), and metadata table (targets) example creation [here](https://github.com/Alexander-Sol/AlsMotorNeuronAnalysis), are study-dependent.
Protein summarization reduces redundancy, stabilizes measurements, and provides interpretable biological units for downstream comparisons.
```r
library(limpa)

# Create EList
y.peptide <- structure(
    list(E = expr, genes = genes, targets = targets),
    class = "EList"
)

# DPC modeling
dpcfit <- dpc(y.peptide)
plotDPC(dpcfit)

# Protein Summarization
y.protein <- dpcQuant(y.peptide, "ProteinGroup", dpc = dpcfit, verbose = TRUE)
```

> Paper: [*Quantification and differential analysis of mass spectrometry proteomics data with probabilistic recovery of information from missing values*](https://www.biorxiv.org/content/10.1101/2025.04.28.651125v1.full)
