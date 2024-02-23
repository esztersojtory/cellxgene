# In Summary

This short introduction aims to show the installation and the setup process for CellxGene and Explore CellxGene. 

It shows how to transform a Seurat object into an .h5ad file as well as the installation instructions for the 2 programs.

# Transform Seurat to .h5ad

Using the SeuratDisk package in R.

```r
library(Seurat)
library(SeuratDisk)

SaveH5Seurat(so, filename = "so.h5Seurat")
Convert("so.h5Seurat", dest = "h5ad")
```
The resulting .h5ad file is compatible with CellxGene and all of its extensions.

# CellxGene

Installation instructions are from the [CellxGene Website](https://cellxgene.cziscience.com/docs/05__Annotate%20and%20Analyze%20Your%20Data/5_1__Getting%20Started:%20Install,%20Launch,%20Quick%20Start).
Python 3.6+ is required and it is recommended to install to a conda/virtual environment.

```
pip intall cellxgene
```

launch from local file in current directory:
```
cellxgene launch example.h5ad --open
```
or from url:
```
cellxgene launch https://cellxgene-example-data.czi.technology/pbmc3k.h5ad
```

CELLxGENE Annotate currently supports the following browsers:

- Google Chrome 61+
- Edge 15+
- Firefox 60+

# exCellxGene

Installation instructions are from the [exCellxGene GitHub](https://github.com/czbiohub-sf/excellxgene).
Python 3.9 is required and it is recommended to install to a conda/virtual environment.

```
conda create -n cxg python=3.9
conda activate cxg
```

Install excellxgene with pip:

```
pip install excellxgene
```

launch from local file in current directory:
```
excellxgene launch example.h5ad --open
```
