# scRNA-Analysis-from-mouse-brain
This project aimed at identifying marker genes that designate cell types based on expression.

# Data
This data is obtained from Kaggle. The scRNA sequencing was done on extracts of the mouse brain. ERCC RNA was used for a technical control. 
Steps followed in the analysis

1. Merge the count and metadata frame into one .AnnData file.
2. Insert a column that describes whether a gene is spike-in or not. Spike in RNAs have a name ID that starts with "ERCC"
3. Calculate the Quality Control metrics from the Scanpy preprocessing library.
4. Filter out cells with a very low number of reads per cell.
5. Filter out cells that expressed genes in very low quantities.
6. Remove cells which contain a high proportion of spike in ERCC counts, e.g.,> 10%.
7. Normalize the filtered data using log or scaling.
8. Extract the highly variable genes and reduce the dimension using PCA.
9. Cluster the cells based on distance and assign labels (k-means).
10. Identify the unique top 10 genes that differentiate the cells from other cell types as markers.

####[<img width="1402" height="574" alt="image" src="https://github.com/user-attachments/assets/71ff47a5-d695-4124-8441-edf92c5b4903" />]

