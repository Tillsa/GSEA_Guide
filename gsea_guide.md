# GSEA Guide
- Cluster profiler documentation:  [https://yulab-smu.github.io/clusterProfiler-book/index.html](https://yulab-smu.github.io/clusterProfiler-book/index.html)
- how to prepare your own gene list: [https://github.com/YuLab-SMU/DOSE/wiki/how-to-prepare-your-own-geneList](https://github.com/YuLab-SMU/DOSE/wiki/how-to-prepare-your-own-geneList)
## make orgdb object
org.db packages are annotation packages that combine gene IDs (Entrez, Locus Tag ...) with ontology IDs (KEGG, GO ...)
- install [AnnotationForge](https://bioconductor.org/packages/release/bioc/html/AnnotationForge.html):
  - open R
  - paste:
  ```
  if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

  BiocManager::install("AnnotationForge")
  ```
  - hit enter and save workspace when asked
