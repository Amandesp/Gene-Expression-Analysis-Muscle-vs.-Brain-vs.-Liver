# Gene Expression Analysis: Muscle vs. Brain vs. Liver

## Executive Summary

Gene expression varies across human tissues because different tissues perform different biological functions. Understanding these differences helps researchers explore how genes are associated with specialized tissue functions.

Using Python, pandas, and Matplotlib, I analyzed publicly available gene expression data from the Genotype-Tissue Expression (GTEx) project. The dataset contains median gene expression measurements across human tissues, measured in transcripts per million (TPM).

The analysis focused on skeletal muscle, brain, and liver tissue. I calculated the average expression across 13 brain regions, filtered genes based on their expression levels across the three tissue categories, and identified the top five genes by skeletal muscle expression among the genes that met the filtering criteria.

The results identified ACTA1, CKM, MYL2, DES, and MT-ND6. ACTA1 and CKM showed particularly high expression in skeletal muscle compared with the average brain and liver measurements.

This project demonstrates how Python can be used to analyze biological data, identify expression patterns, and visualize differences across tissue types.

## Research Question

Which genes have the highest expression in skeletal muscle compared to brain and liver tissue?

### Objectives

- Compare gene expression levels across skeletal muscle, brain, and liver.
- Calculate average expression across selected brain regions.
- Identify genes with higher skeletal muscle expression than both the average brain and liver measurements.
- Rank the selected genes by skeletal muscle expression.
- Visualize differences in expression using Python.
- Interpret the results while recognizing the limitations of the analysis.

## Dataset

The data comes from the Genotype-Tissue Expression (GTEx) project, which provides publicly available information about gene expression across human tissues.

**Dataset:** `GTEx_Analysis_2017-06-05_v8_RNASeQCv1.1.9_gene_median_tpm.txt`

**Source:** [GTEx Portal – Adult GTEx Downloads](https://www.gtexportal.org/home/downloads/adult-gtex/bulk_tissue_expression)

The dataset used in this project contains 56,200 rows and 56 columns, including gene identifiers, gene symbols, and expression measurements across 54 tissue categories.

**Key measurement:**

- **TPM (Transcripts Per Million):** A normalized measure of RNA abundance used to quantify gene expression.

**Tissues analyzed:**

- Skeletal muscle
- 13 brain regions, summarized using their average expression per gene
- Liver

## Research Motivation

Different tissues have different biological functions and can exhibit distinct gene expression patterns. Comparing expression levels across tissues provides a way to explore these differences using data analysis.

This project investigates the following questions:

- Which genes have the highest skeletal muscle expression among genes meeting the filtering criteria?
- How do their expression levels compare with average brain and liver expression?
- Which selected genes show the largest differences between tissues?
- How do the observed patterns relate to the known biological functions of these genes?

The goal was to use Python to identify, compare, and visualize tissue-associated gene expression patterns.

## Methodology

1. Loaded the GTEx gene median TPM dataset into Python using pandas.
2. Examined the dataset dimensions and available tissue columns.
3. Selected skeletal muscle, brain, and liver expression measurements.
4. Calculated the average expression across 13 brain regions for each gene.
5. Filtered the dataset to retain genes with skeletal muscle expression greater than both average brain expression and liver expression.
6. Identified 6,549 genes that met the filtering criteria.
7. Ranked the filtered genes by skeletal muscle expression and selected the top five.
8. Created a grouped bar chart using Matplotlib to compare expression across skeletal muscle, average brain, and liver.
9. Used a logarithmic y-axis to visualize expression values spanning a wide range.
10. Exported the selected results to a CSV file for further use.

## Skills

**Python:** Data analysis, data manipulation, filtering, sorting, working with tabular datasets

**Pandas:** Data loading, column selection, data transformation, averaging, conditional filtering, ranking, CSV export

**Matplotlib:** Data visualization, grouped bar charts, logarithmic scales, chart labeling

**Data Analysis:** Exploratory data analysis (EDA), comparative analysis, pattern identification, interpreting results, documenting limitations

**Research Skills:** Working with public scientific datasets, developing research questions, interpreting biological measurements, communicating findings

## Results & Findings

The analysis identified the following five genes with the highest skeletal muscle expression among genes that met the filtering criteria.

| Gene | Skeletal Muscle (TPM) | Average Brain (TPM) | Liver (TPM) |
|---|---:|---:|---:|
| ACTA1 | 33,847.5 | 4.836 | 1.967 |
| CKM | 25,785.6 | 2.014 | 1.305 |
| MYL2 | 12,092.5 | 1.792 | 1.324 |
| DES | 12,069.4 | 4.629 | 5.181 |
| MT-ND6 | 11,686.1 | 8,565.504 | 5,021.890 |

### Key Findings

**1. ACTA1 showed the highest skeletal muscle expression among the selected genes.**

ACTA1 had approximately 33,847.5 TPM in skeletal muscle, compared with much lower expression in average brain and liver. ACTA1 encodes a skeletal muscle alpha-actin protein associated with muscle structure and function.

**2. CKM also showed particularly high skeletal muscle expression.**

CKM had approximately 25,785.6 TPM in skeletal muscle. The gene encodes muscle creatine kinase, which plays an important role in energy metabolism during muscle activity.

**3. MYL2 and DES showed substantially higher expression in skeletal muscle.**

MYL2 is associated with the regulation of muscle contraction, while DES encodes desmin, a structural protein involved in maintaining muscle cell organization.

**4. MT-ND6 showed expression across all three tissue categories.**

MT-ND6 had approximately 11,686.1 TPM in skeletal muscle, 8,565.5 TPM in average brain, and 5,021.9 TPM in liver. Although its expression was highest in skeletal muscle among these three measurements, it was also highly expressed in brain and liver.

**5. The visualization highlighted differences in expression levels.**

The grouped bar chart compared expression across skeletal muscle, average brain, and liver. A logarithmic y-axis made it easier to visualize measurements that differed substantially in magnitude.

Overall, the results demonstrate that some genes have considerably higher expression in skeletal muscle than in the other tissue measurements examined.

These findings describe observed expression patterns and do not establish statistical significance or prove that the selected genes are exclusive to skeletal muscle.

## Biological Interpretation

The selected genes include examples associated with muscle structure, contraction, and energy metabolism.

ACTA1 and DES are associated with muscle structure, while CKM and MYL2 are involved in processes related to muscle function. MT-ND6 encodes a component of mitochondrial complex I, which participates in cellular energy production.

The observed differences illustrate how gene expression can vary across tissues with different biological functions. However, gene expression measurements alone do not fully explain a gene's function or establish that a gene acts exclusively in one tissue.

## Limitations

- The analysis uses median gene expression measurements rather than individual-level expression data.
- Averaging 13 brain regions may obscure differences between individual regions.
- The filtering criteria identify genes with higher expression in skeletal muscle than in average brain and liver; this does not establish that the genes are muscle-specific.
- The analysis does not include statistical significance testing or differential expression analysis.
- The top five genes are ranked by skeletal muscle expression among the filtered genes, not by a formal tissue-specificity metric.
- The findings depend on the selected tissues, dataset, and filtering criteria.
- Observed expression differences do not establish causation or fully explain biological function.

## Next Steps

1. Create a heatmap to compare expression patterns across a larger selection of genes and tissues.
2. Investigate expression differences across individual brain regions.
3. Explore tissue-specificity metrics to identify genes with more restricted expression patterns.
4. Use appropriate statistical methods with suitable sample-level data to investigate expression differences.
5. Expand the analysis to additional tissues to explore broader expression patterns.
6. Improve visualizations to communicate the results more effectively.

## Tools & Technologies

- Python
- pandas
- Matplotlib
- Jupyter Notebook
- GTEx gene expression dataset

## Data Source

[GTEx Portal – Adult GTEx Bulk Tissue Expression Data](https://www.gtexportal.org/home/downloads/adult-gtex/bulk_tissue_expression)

The GTEx project provides gene expression data across human tissues to support research into tissue biology and gene regulation.

## Conclusion

This project used Python to investigate gene expression differences between skeletal muscle, brain, and liver. By averaging expression across brain regions, filtering the dataset, and ranking genes by skeletal muscle expression, I identified five genes with higher expression in skeletal muscle than in the other two comparisons.

The results highlighted particularly high skeletal muscle expression for ACTA1 and CKM, along with expression patterns for MYL2, DES, and MT-ND6.

The project demonstrates practical experience with Python-based data analysis, data manipulation, comparative visualization, and scientific interpretation. It also highlights the importance of accurately describing analytical methods and acknowledging limitations when interpreting data.
