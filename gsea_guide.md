# GSEA Guide
- Cluster profiler documentation:  [https://yulab-smu.github.io/clusterProfiler-book/index.html](https://yulab-smu.github.io/clusterProfiler-book/index.html)
- how to prepare your own gene list: [https://github.com/YuLab-SMU/DOSE/wiki/how-to-prepare-your-own-geneList](https://github.com/YuLab-SMU/DOSE/wiki/how-to-prepare-your-own-geneList)
## make org.db object
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
- install GO.db:
  - open R
  - paste:
  ```
  if (!requireNamespace("BiocManager", quietly = TRUE))
      install.packages("BiocManager")

  BiocManager::install("GO.db")
  ```
  - hit enter and save workspace when asked
- run the following R code (write to a script and run with Rscript)  
  the tax_id (taxonomy ID) can be searched at [https://www.ncbi.nlm.nih.gov/Taxonomy/taxonomyhome.html/](https://www.ncbi.nlm.nih.gov/Taxonomy/taxonomyhome.html/)

  ```
  library('AnnotationForge')
  makeOrgPackageFromNCBI(version = "0.1",
                       author = "Till Sauerwein <till-sauerwein@email.de>",
                       maintainer = "Till Sauerwein <till-sauerwein@email.de>",
                       outputDir = "data",
                       tax_id = "93061",
                       genus = "Staphylococcus",
                       species = "Staphylococcusaureus")

  ```

# KEGG Genome ID
for a complete list of supported organism ids go to http://www.genome.jp/kegg/catalog/org_list.html 

# install clusterprofiler
 - open R
  - paste:
```
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("clusterProfiler")

```
 - hit enter and save workspace when asked
