# miRsense_OFF
Supplementary code for Master Thesis "miRsense OFF: a dynamic disease-driven gene therapy for epilepsy"

In this repository, all code used in the Master Thesis is displayed. A short description of the respective files and how they are used in the analysis is provided here. Data files (ABF files, csv files, .tiff files) should be stored locally and not on github. If datafolders are stored within your repository, add these folders to 'gitignore' 

ABF_analysis:
Analysis of Axon Binary Files obtained from whole-cell voltage-clamp recordings using pyABF. Baseline is averaged and subtracted from the current traces using numpy. Mean maximum current is calculated based on 100 ms range in the center of the voltage step using numpy. Data is stored in .csv file. 

Anova:
Two-way ANOVA for repeated measurements using statsmodels ols. Posthoc Tukey's HSD comparing timepoints and conditions.

Bargraphs:
Creates bargraph comparing two groups represented in pandas dataframes. Errorbars set to SEM. Seaborn and Matplotlib pyplot used. 

Boxplot:
Creates boxplots comparing two or more groups represented in .csv files using seaborn, pandas and matplotlib pyplot

IV_curves:
Two parts for either single or multiple I/V curves in one graphic. Reads in .csv file and creates I/V curve with error bars rerpesenting SEM. Used after primary ABF_analysis.

MWU_and_T_test:
Scipy Mann-Whitney-U test comparing two groups defined in the code. 

Normality_test:
Uses Shapiro-Wilk test from scipy to inspect normality of data groups provided in .csv file. 

PCC_and_rsquared:
Uses scipy pearsonr and numpy to calculate PCC, r², and CV of dataset provided in .csv file. 

Image_processing_pipelin:
Pipeline that reads in .tiff files from fluorescence imaging, renames the files according to the order in which they are acquired and performs integrated density calculation and minimum subtraction. Output is saved in .csv file. Uses numpy, skimage and pandas. 

Traces:
Two parts, either displaying single or multiple current traces from ABF files in graphic. Uses pyabf, matplotlib pyplot and numpy
