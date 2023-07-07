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
