# G-S-M-V

G-S-M V tool incorporates several PBK databases into multi-omics  data analysis by utilizing supervised ML and statistical methods. The first objective of the tool is to integrate multi omics datasets utilizing scoring and ranking information over  the iterations. Our study aims to track the scores of each group across multiple iterations so that score vectors with a length of 100 are generated for the groups. These score vectors are used to identify hidden patterns among the groups.

# Data Preparation

The two omics-datasets (BRCA miRNA and mRNA gene  expression profiles) are given as input data into the workflow. While columns represent the features and class information, rows contains sample IDs. The binary class (case and control or subtypes of the interested disease) information is given as string in each input datasets with ".table" extension files.

# Main workflow

![alt text](https://github.com/malikyousef/G-S-M-V/blob/main/Images/G-S-M-V_main_workflow.JPG?raw=true)

# Parameters

The SetParameters node allows the users to change the parameters.

* Positive Correlation Threshold (Default: 0.6)
* Negative Correlation Threshold (Default: -0.6)
* Number of iteration (Default: 100)
* Number of Group (Default: 10)
* Number of iterations for Internal Rank (Default: 10)
* Performance metric (Accuracy, Precision, Sensitivity, etc.) weight (Default for accuracy: 1.0)

![alt text](https://github.com/malikyousef/G-S-M-V/blob/main/Images/G-S-M-V_approach.JPG?raw=true)


# The Environment Settings 

After installing KNIME Analytics platform, G-S-M-V workflow is downloaded and imported into the KNIME. The workflow contains R scripts therefore the following commands should be followed to prevent errors. Before initiation of the workflow process in KNIME, R / RStudio is required to be run with following commands:

library(Rserve);
Rserve(args = "--vanilla")
library(tidyr)

# Identification of Significant Groups

![alt text](https://github.com/malikyousef/G-S-M-V/blob/main/Images/Significant_group_summary_statistics.JPG?raw=true)

Significant Groups summarizes different characteristics of the significant groups. Frequency of the groups over  100 iterations are given under the column ‘Frequency of  Group’. The average scores and ranks of each group calculated  within the S component are given in the following two columns  of the table. # Associated Genes and Associated Genes  represent the number and set of unique target genes of each  group respectively. Iteration and rank information tracked via  MCCV are given as lists in the last two columns. 



