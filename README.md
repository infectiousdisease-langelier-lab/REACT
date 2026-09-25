# Culture-benchmarked metagenomics maps microbial strain sharing in long-term acute care

This repository contains the code for the paper **Culture-benchmarked metagenomics maps microbial strain sharing in long-term acute care**.

## Code

REACT_analysis.Rmd is used to analyze the data and produce manuscript figures 1-3 and 5, supplementary tables 1-3, and supplementary figures 1-9. This code uses the following input files: 

Data Files:
* [patients.csv](../DataFiles/patients.csv)
* [samples.csv](../DataFiles/samples.csv)
* [rooms.csv](../DataFiles/rooms.csv)
* [providers.csv](../DataFiles/providers.csv)
* [micro_cultures_filt.csv](../DataFiles/micro_cultures_filt.csv)
* [mNGS_samples.csv](../DataFiles/mNGS_samples.csv)
* [SOI_instrain_newthreshold.csv](../DataFiles/SOI_instrain_newthreshold.csv)
* [SOI_instrain_oldthreshold.csv](../DataFiles/SOI_instrain_oldthreshold.csv)
* [MAGs_SOI.csv](../DataFiles/MAGs_SOI.csv)
* [MAGs_all.csv](../DataFiles/MAGs_all.csv)
* [MAGs_all_filt.csv](../DataFiles/MAGs_all_filt.csv)
* [MAGs_amr.csv](../DataFiles/MAGs_amr.csv)
* [strain_sharing_samples.csv](../DataFiles/strain_sharing_samples.csv)

Phylogenetic Tree Files:
* [Acinetobacter_tree.newick](../REACTTree/Acinetobacter_tree.newick)
* [Cdiff_tree.nwk](../REACTTree/Cdiff_tree.nwk)
* [Citrobacter_tree.nwk](../REACTTree/Citrobacter_tree.nwk)
* [Cperfingens_tree.nwk](../REACTTree/Cperfingens_tree.nwk)
* [ecoli_phylo_tree_0326.nwk](../REACTTree/ecoli_phylo_tree_0326.nwk)
* [Efaecalis_tree.nwk](../REACTTree/Efaecalis_tree.nwk)
* [Efaecium_tree.nwk](../REACTTree/Efaecium_tree.nwk)
* [Enterobacter_spp_phylo_tree_0326.nwk](../REACTTree/Enterobacter_spp_phylo_tree_0326.nwk)
* [Klebspp_tree.nwk](../REACTTree/Klebspp_tree.nwk)
* [Kpneumo_tree.nwk](../REACTTree/Kpneumo_tree.nwk)
* [Paeruginosa_tree.nwk](../REACTTree/Paeruginosa_tree.nwk)
* [Pmirabilis_tree.nwk](../REACTTree/Pmirabilis_tree.nwk)
* [Smaltophilia_tree.nwk](../REACTTree/Smaltophilia_tree.nwk)

## Input

Data Files:
* [patients.csv](../DataFiles/patients.csv): Metadata on each patient
* [samples.csv](../DataFiles/samples.csv): Metadata on each sample
* [rooms.csv](../DataFiles/rooms.csv): Room location of each patient at different timepoints
* [providers.csv](../DataFiles/providers.csv): Hand hygiene data of providers
* [micro_cultures_filt.csv](../DataFiles/micro_cultures_filt.csv): MDRO culture results
* [mNGS_samples.csv](../DataFiles/mNGS_samples.csv): mNGS sequencing results
* [SOI_instrain_newthreshold.csv](../DataFiles/SOI_instrain_newthreshold.csv): inStrain compare dataset of the all mNGS and WGS samples using the derep MAGs and the original thresholds for "shared strain"
* [SOI_instrain_oldthreshold.csv](../DataFiles/SOI_instrain_oldthreshold.csv): inStrain compare dataset of the all mNGS and WGS samples using the derep MAGs and the new thresholds for "shared strain"
* [MAGs_SOI.csv](../DataFiles/MAGs_SOI.csv): Presence/absence MAGs dataset of species of interest detected in the mNGS samples
* [MAGs_all.csv](../DataFiles/MAGs_all.csv): All MAGs detected in the mNGS samples (including unused donor stool doses)
* [MAGs_all_filt.csv](../DataFiles/MAGs_all_filt.csv): Filtered MAGs detected in the mNGS samples (excluding unused donor stool doses)
* [MAGs_amr.csv](../DataFiles/MAGs_amr.csv): AMR genes detected on MAGs
* [strain_sharing_samples.csv](../DataFiles/strain_sharing_samples.csv): Strain-sharing rates between paired samples

Phylogenetic Tree Files: WGS of MDRO culture isolates by bacterial species
* [Acinetobacter_tree.newick](../REACTTree/Acinetobacter_tree.newick): Acinetobacter baumannii WGSs
* [Cdiff_tree.nwk](../REACTTree/Cdiff_tree.nwk): Clostridioides difficile WGSs
* [Citrobacter_tree.nwk](../REACTTree/Citrobacter_tree.nwk): Citrobacter freunii WGSs
* [Cperfingens_tree.nwk](../REACTTree/Cperfingens_tree.nwk): Clostridium perfringens WGSs
* [ecoli_phylo_tree_0326.nwk](../REACTTree/ecoli_phylo_tree_0326.nwk): Escherichia coli WGSs
* [Efaecalis_tree.nwk](../REACTTree/Efaecalis_tree.nwk): Enterococcus faecalis WGSs
* [Efaecium_tree.nwk](../REACTTree/Efaecium_tree.nwk): Enterococcus faecium WGSs
* [Enterobacter_spp_phylo_tree_0326.nwk](../REACTTree/Enterobacter_spp_phylo_tree_0326.nwk): Enterobacter species WGSs
* [Klebspp_tree.nwk](../REACTTree/Klebspp_tree.nwk): non-Klebsiella pnuemoniae Klebsiella species WGSs
* [Kpneumo_tree.nwk](../REACTTree/Kpneumo_tree.nwk): Klebsiella pneumoniae WGSs
* [Paeruginosa_tree.nwk](../REACTTree/Paeruginosa_tree.nwk): Pseudomonas aeruginosa WGSs
* [Pmirabilis_tree.nwk](../REACTTree/Pmirabilis_tree.nwk): Proteus mirabilis WGSs
* [Smaltophilia_tree.nwk](../REACTTree/Smaltophilia_tree.nwk): Stenotrophomonas maltophilia WGSs

## Required hardware and software dependencies

The codes were run on a Mac laptop. The required R packages (see below for more details) could be installed with the command `install.package()` and `BiocManager::install()`. Each package can take up to 1 minute to install. Please refer to each package's website for more information on the installation.

```
R version 4.2.1 (2022-06-23)
Platform: x86_64-apple-darwin17.0 (64-bit)
Running under: macOS 26.5.2

Matrix products: default
LAPACK: /Library/Frameworks/R.framework/Versions/4.2/Resources/lib/libRlapack.dylib

locale:
[1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8

attached base packages:
[1] grid      stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] circlize_0.4.17       ComplexHeatmap_2.14.0 ape_5.7-1             vegan_2.6-4           lattice_0.22-7        permute_0.9-8        
 [7] ggnewscale_0.5.2      ggtreeExtra_1.8.1     tidygraph_1.3.0       ggraph_2.1.0          ggtree_3.6.2          igraph_1.5.1         
[13] viridis_0.6.5         viridisLite_0.4.2     gridExtra_2.3         patchwork_1.3.2       ggrepel_0.9.4         scales_1.4.0         
[19] lubridate_1.9.4       forcats_1.0.1         stringr_1.6.0         dplyr_1.1.4           purrr_1.2.0           readr_2.1.4          
[25] tidyr_1.3.0           tibble_3.3.0          ggplot2_4.0.1         tidyverse_2.0.0       car_3.1-3             carData_3.0-5        
[31] glmmTMB_1.1.8         geepack_1.3.9         gtsummary_2.4.0      

loaded via a namespace (and not attached):
 [1] colorspace_2.1-2    TH.data_1.1-5       minqa_1.2.6         rjson_0.2.23        estimability_1.5.1  GlobalOptions_0.1.3 fs_1.6.6           
 [8] aplot_0.2.9         clue_0.3-66         rstudioapi_0.17.1   farver_2.1.2        graphlayouts_1.0.1  mvtnorm_1.2-4       codetools_0.2-20   
[15] splines_4.2.1       doParallel_1.0.17   knitr_1.50          polyclip_1.10-7     Formula_1.2-5       jsonlite_2.0.0      nloptr_2.0.3       
[22] broom_1.0.10        cluster_2.1.8.1     png_0.1-8           ggforce_0.4.1       compiler_4.2.1      emmeans_2.0.0       backports_1.5.0    
[29] Matrix_1.6-4        fastmap_1.2.0       lazyeval_0.2.2      cli_3.6.5           tweenr_2.0.3        htmltools_0.5.8.1   tools_4.2.1        
[36] coda_0.19-4.1       gtable_0.3.6        glue_1.8.0          rappdirs_0.3.3      Rcpp_1.1.0          vctrs_0.6.5         nlme_3.1-164       
[43] iterators_1.0.14    xfun_0.54           lme4_1.1-35.1       timechange_0.3.0    lifecycle_1.0.4     MASS_7.3-58.1       zoo_1.8-14         
[50] hms_1.1.4           parallel_4.2.1      sandwich_3.1-1      TMB_1.9.10          RColorBrewer_1.1-3  yaml_2.3.10         ggfun_0.2.0        
[57] yulab.utils_0.2.1   stringi_1.8.7       S4Vectors_0.36.2    foreach_1.5.2       tidytree_0.4.6      BiocGenerics_0.44.0 boot_1.3-32        
[64] shape_1.4.6.1       matrixStats_1.5.0   rlang_1.1.6         pkgconfig_2.0.3     evaluate_1.0.5      treeio_1.22.0       cowplot_1.2.0      
[71] tidyselect_1.2.1    magrittr_2.0.4      R6_2.6.1            IRanges_2.32.0      generics_0.1.4      multcomp_1.4-29     pillar_1.11.1      
[78] withr_3.0.2         mgcv_1.9-1          survival_3.8-3      abind_1.4-8         crayon_1.5.3        tzdb_0.5.0          rmarkdown_2.30     
[85] GetoptLong_1.1.0    S7_0.2.1            digest_0.6.37       xtable_1.8-4        numDeriv_2016.8-1.1 gridGraphics_0.5-1  stats4_4.2.1       
[92] ggplotify_0.1.3

```
