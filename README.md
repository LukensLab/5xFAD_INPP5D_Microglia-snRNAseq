# 5xFAD_INPP5D_Microglia-snRNAseq
Workflow and R code used for the analysis of snRNAseq data comparing 5xFAD INPP5D vs 5xFAD.  

R code provided. Two experimental groups: 5xFAD INPP5D Microglia (5xBOAT) and 5xFAD.


The R folder contains the R code used in the workflow to process and analyze the 5xBOAT and 5xFAD snRNAseq samples. The full list of packages and versions at the time the analysis was conduced can be found in the RStudio_Packages_and_Versions file.


## Mouse INPP5D snRNAseq workflow:
1. R/5xBOAT_snRNAseq_QC_and_Integration.Rmd
- Follows steps for data input into RStudio, QC, and SCTransform (normalization and integration).

2. R/5xBOAT_snRNAseq_Clustering.Rmd
- Follows steps for PCA, UMAP clustering, and identification of clusters. Ends with the subsetting of the Microglia and Neuron clusters.

3. R/5xBOAT_snRNAseq_Subclustering.Rmd
- Follows steps for the re-clustering of the Microglia cluster. Begins with stripping the metadata from the Microglia cluster, then follows steps to repeat SCTransform (normalization and integration), PCA, UMAP clustering, and identification of microglia Subpopulations.

4. R/5xBOAT_snRNAseq_DE_Analysis.Rmd
- Follows steps for differential gene expression testing using Seuart and DESeq2. Ends with the visualization of differentially expressed genes by volcano plot. 

5. R/5xBOAT_snRNAseq_Data_Visualization.Rmd
- Follows code for other data visualizations including Heatmap and DotPlot.

6. R/RStudio_PackageAndVersionExtraction.Rmd
- Follwos code for the extraction of packages and versions from RStudio.
