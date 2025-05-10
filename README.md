# Differential-Expression-anf-Functional-Enrichment-
This analysis investigates transcriptional changes between control and treatment conditions (likely drug vs. vehicle) using RNA-seq count data.
The pipeline consists of several key steps:

Data Preparation:

Raw count and FPKM data were loaded.

Genes with low expression were filtered out by retaining only those with counts >20 in any sample.

Distribution of log2-transformed expression values was visualized.

Differential Expression Analysis:

A DESeq2 object was created using a metadata table defining control and treatment groups.

DESeq2 normalization and statistical testing identified differentially expressed genes (DEGs).

Significant DEGs were filtered at adjusted p-value < 0.01.

Top upregulated and downregulated genes were extracted.

Visualization:

A heatmap of significant DEGs was generated using Z-score-normalized expression values.

A volcano plot was created to display fold change versus significance, highlighting key DEGs.

Functional Enrichment (GO) Analysis:

Gene Ontology (GO) annotations were loaded from PlasmoDB.

Custom scripts were used to test for GO term enrichment among upregulated genes.

GO terms with padj < 0.01 were selected as significantly enriched.

A horizontal barplot visualized enriched biological processes.

