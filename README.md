# R2-D2-model
R2-D2 model is a statistical method to identify the potential regulatory genetic variants to a gene. (add more description here once it is published).

#### If you find our model useful in your research, please cite:

(XXXXXXX)

### Table of Contents

#### 1. [Prepare input files](#prepare-input-files)
#### 2. [Download the scripts in this repository](https://github.com/saffenlab/R2-D2-model.git)
#### 3. [Run the R2-D2 model](#run-the-r2-d2-main-program)
#### 4. [Generate R2-D2 plots](#generate-the-r2-d2-plots)


## Prepare input files
Three types of input files are needed to run this model. 

    1. Genotype file which describes the SNP genotypes for a group of individuals. It can be generated by [PLINK](http://zzz.bwh.harvard.edu/plink/).  
    2. Phenotype file. This should be three-column text files, of which the first two columns are family ID (FID), and individual IDs (IID), and the third column 
    3. Genotype-Phenotype association results. This is also a standard output from PLINK. It listed useful metrics of genotype-phenotype associations, such as P-value, R-squared, and direction of effect.

## Run the R2-D2 main program
    This is done by running the comTest_matrix() function in the protocol.R file
    comTest_matrix(geno = , qassoc = , num = 4, save_interm = T)
    Paramters:
      -- geno: the genotype file
      -- qassoc: the genotype-phenotype association file
      -- num: number of SNPs in a SNP combination to be exaustively tested
      -- save_interm: whether or not to save the intermediate files, useful for checking model
      
      
## Generate the R2-D2 plots
    This is done by running the familyPlot_matrix() function in the protocol.R file
    familyPlot_matrix(plot_file = , title = , color = c("red", "green", "black")) 
    Paramters:
      -- plot_file: input file generated by the comTest_matrix()
      -- title: title to be displayed in the plots, also used as output filename
      -- color: colors for the SNPs chosen by the model.

## Example
