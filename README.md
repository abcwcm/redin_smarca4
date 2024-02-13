
# SMARCA4 controls state plasticity in small cell lung cancer through regulation of neuroendocrine transcription factors and REST splicing

Script related to the analysis of single cell transcriptomic data by **Redin et al.** using data from Ireland et al.


![](WCM_MB_LOGO_HZSS1L_CLR_RGB_new.png)

## DATA AVAILABILITY
* Processed data was obtained via personal communication from Ireland et al.
## DATA ANALYSIS

ABC received the processed monocle2 cellular trajectory prediction object from Ireland et al. (Figure 4D) in which normalized expression values, pseudotime projections and neuro endocrine (NE) scores based on Zhang et al. signatures were included. Using the normalized expression values of RPM1-4 a Seurat object was created, data was scaled using ScaleData function, dimensionality reduction was applied using RunPCA, cellular neighbors were found by FindNeighbors function using the first 20 PCA and clusters were identified by Louvain approach (FindClusters, resolution=0.5) (Satija et al.). 2D embedding was performed using tSNE approach (RunTSNE, dim=20) and cellular clusters were plotted. Using these embedded coordinates, Smarca4 log transformed values as well as NE scores were plotted for each RPM cells. Similarly, log expression values for Smarca4 and Smarca2 (or any other gene), as well as, NE scores for each cell were plotted using previously computed pseudotime profiles by Ireland et al. All these steps were run following [pseudotime_data.Rmd](https://github.com/abcwcm/redin_smarca4/blob/main/analysis_scripts/Pseudotime_Redin_Ireland-data.Rmd) script. 

## REFERENCES
* Ireland, AS, Micinski, AM, Kastner, DW, Guo, B, Wait, SJ, Spainhower, KB, Conley, CC, Chen, OS, Guthrie, MR, Soltero, D, Qiao, Y, Huang, X, k, S, Devarakonda, S, Chalishazar, MD, Gertz, J, Moser, JC, Marth, G, Puri, S, Witt, BL, Spike, BT, Oliver, TG (2020). MYC Drives Temporal Evolution of Small Cell Lung Cancer Subtypes by Reprogramming Neuroendocrine Fate. Cancer Cell, 38, 1:60-78.e12.
* Zhang, W, Girard, L, Zhang, YA, Haruki, T, Papari-Zareei, M, Stastny, V, Ghayee, HK, Pacak, K, Oliver, TG, Minna, JD, Gazdar, AF (2018). Small cell lung cancer tumors and preclinical models display heterogeneity of neuroendocrine phenotypes. Transl Lung Cancer Res, 7, 1:32-49.
* Satija, R, Farrell, JA, Gennert, D, Schier, AF, Regev, A (2015). Spatial reconstruction of single-cell gene expression data. Nat Biotechnol, 33, 5:495-502.