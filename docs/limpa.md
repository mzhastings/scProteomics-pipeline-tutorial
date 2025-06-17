# Differential Expression with limpa

## Installation
```r
devtools::install_github("nesvilab/limpa")
```

## Usage
```r
library(limpa)
res <- limpa(data_matrix, design_matrix)
```
- Uses empirical Bayes shrinkage and probabilistic imputation

> Paper: *Quantification and differential analysis of mass spectrometry proteomics data with probabilistic recovery of information from missing values*
