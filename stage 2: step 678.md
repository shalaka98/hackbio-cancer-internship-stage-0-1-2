### step 1: install package
```
install.packges()
```
### step 2: import file

```
glioblastoma <- read.csv("https://raw.githubusercontent.com/HackBio-Internship/public_datasets/main/Cancer2024/glioblastoma.csv")
```
### step 3: subsetting
> referencing: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7859841/
###### keep only the significant genes
results_sig = subset(results, padj < 0.05)
###### get the significant up-regulated genes
up = subset(results_sig, log2FoldChange > 0)
###### get the significant down-regulated genes
down = subset(results_sig, log2FoldChange < 0)


> referring AI
```
downregulated_genes <- data_matrix[rowMeans(data_matrix) < -fold_change_cutoff & p_values < p_value_cutoff, ]
upregulated_genes <- data_matrix[rowMeans(data_matrix) > fold_change_cutoff & p_values < p_value_cutoff, ]
```
