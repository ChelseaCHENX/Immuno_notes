# Notes on Immunology-related tools and databases

* [Notes](#notes)
* [Data](#-data-)
* [Web-based tools](#web)
* [Stand-alone tools](#tools)

## Notes

- Spranger, Stefani, Jason J. Luke, Riyue Bao, Yuanyuan Zha, Kyle M. Hernandez, Yan Li, Alexander P. Gajewski, Jorge Andrade, and Thomas F. Gajewski. “Density of Immunogenic Antigens Does Not Explain the Presence or Absence of the T-Cell-Inflamed Tumor Microenvironment in Melanoma.” Proceedings of the National Academy of Sciences of the United States of America 113, no. 48 (29 2016): E7759–68. https://doi.org/10.1073/pnas.1609376113.
    - **T cell signature**: CD8A, CCL2, CCL3, CCL4, CXCL9, CXCL10, ICOS, GZMK, IRF1, HLA-DMA, HLA-DMB, HLA-DOA, and HLA-DOB
    - **CTNNB1 score**: mean expression of TCF1, TCF12, MYC, EFNB3, VEGFA, and APC2, to be correlated with CD8b expression

## `data`

- `EINAV_INTERFERON_SIGNATURE_IN_CANCER.txt` - A gene expression signature found in a subset of cancer patients suggestive of a deregulated immune or inflammatory response. http://software.broadinstitute.org/gsea/msigdb/geneset_page.jsp?geneSetName=EINAV_INTERFERON_SIGNATURE_IN_CANCER

#### `BRCA`

Data from Azizi, Elham, Ambrose J. Carr, George Plitas, Andrew E. Cornish, Catherine Konopacki, Sandhya Prabhakaran, Juozas Nainys, et al. “Single-Cell Immune Map of Breast Carcinoma Reveals Diverse Phenotypic States Driven by the Tumor Microenvironment.” BioRxiv, January 1, 2017. https://doi.org/10.1101/221994. - scRNA-seq of immune cells in BRCA. inDrop single-cell technology. SEQC processing pipeline, Bisquit Bayesian clustering and normalization that removes confounding technical effects. Heterogeneity of immune cell composition, clusters of immune cell subpopulations, covariance among them. Supplementary Material at https://www.biorxiv.org/content/early/2017/11/25/221994.figures-only

- `221994-2.xlsx` - Table S2. Annotations of clusters inferred in full breast immune atlas (across all patients and tissues) and their proportions across tissues and patients.

- `221994-3.xlsx` - Table S3. List of differentially expressed genes in clusters listed in Table S2 (sheet 1); the subset of differentially expressed immune-related genes (sheet 2).

- `221994-2.xlsx` - Table S4. List of gene signatures (sources listed in STAR Methods)

#### `Cibersort`

Data from Newman, Aaron M., Chih Long Liu, Michael R. Green, Andrew J. Gentles, Weiguo Feng, Yue Xu, Chuong D. Hoang, Maximilian Diehn, and Ash A. Alizadeh. “Robust Enumeration of Cell Subsets from Tissue Expression Profiles.” Nature Methods 12, no. 5 (May 2015): 453–57. https://doi.org/10.1038/nmeth.3337. - CIBERSORT - cell type identification. Support Vector Regression. Methods description. Non-log-linear space. p-value for the overall goodness of deconvolution (H0 - no cell types are present in a given gene expression profile), also Pearson and RMSE for estimating goodness of fit. https://cibersort.stanford.edu/index.php

- `LM22.txt` - 547 genes X 22 immune cell types matrix of cell type specific gene signatures


#### `ESTIMATE`

Yoshihara, Kosuke, Maria Shahmoradgoli, Emmanuel Martínez, Rahulsimham Vegesna, Hoon Kim, Wandaliz Torres-Garcia, Victor Treviño, et al. “Inferring Tumour Purity and Stromal and Immune Cell Admixture from Expression Data.” Nature Communications 4 (2013): 2612. doi:10.1038/ncomms3612. https://www.nature.com/articles/ncomms3612#supplementary-information

- `ncomms3612-s2.xlsx` - A gene list of stromal and immune signatures
- `ncomms3612-s3.xlsx` - A list of stromal, immune, and ESTIMATE scores in TCGA data sets. All cancers, all gene expression plaforms.

#### `ImmQuant` data

- Frishberg, Amit, Avital Brodt, Yael Steuerman, and Irit Gat-Viks. “ImmQuant: A User-Friendly Tool for Inferring Immune Cell-Type Composition from Gene-Expression Data.” Bioinformatics 32, no. 24 (December 15, 2016): 3842–43. https://doi.org/10.1093/bioinformatics/btw535. - Deconvolution of immune cell lineages. http://csgi.tau.ac.il/ImmQuant/downloads.html

The log2-scaled reference data files. http://csgi.tau.ac.il/ImmQuant/download.html  

- `ImmGen.txt` - mouse reference data (Heng and Painter, 2008)
- `DMAP.txt` - human reference data (Novershtern et al., 2011)
- `IRIS.txt` - human reference data (Abbas et al., 2005)

#### `quanTIseq` data

- Finotello, Francesca, Clemens Mayer, Christina Plattner, Gerhard Laschober, Dietmar Rieder, Hubert Hackl, Anne Krogsdam, et al. “QuanTIseq: Quantifying Immune Contexture of Human Tumors.” BioRxiv, January 1, 2017. https://doi.org/10.1101/223180. https://www.biorxiv.org/content/early/2017/11/22/223180

- `223180-4.xlsx` - Immune cell signatures, 170 genes x 10 immune cell types. [Source](https://www.biorxiv.org/highwire/filestream/68173/field_highwire_adjunct_files/3/223180-4.xlsx)


## `web`

- `Haemosphere` - mostly murine immune cell signatures, downloadable data. http://haemosphere.org/datasets/show
 
- `TCIA` - The Cancer Immunome Atlas, https://tcia.at/home. Immunophenograms, cell type fraction table of TCGA samples. Survival analysis based on immune cell signatures. All analyses are on TCGA data.

- `TIMER` - immune cell-oriented exploration of TCGA cancers. Six analysis modules: Gene correlation with immune cell proportions, immune proportions and survival, and mutations, and somatic copy number alterations, simple boxplot expression of a gene across all cancer/normal samples, correlation between two genes adjusted for tumor purity or age, deconvolution of user-provided gene expression, estimation of immune proportions in all TCGA samples. https://cistrome.shinyapps.io/timer/ 


## `tools`

#### `ImmQuant`

Download from http://csgi.tau.ac.il/ImmQuant/download.html, run as `java -jar ImmQuant.jar`


