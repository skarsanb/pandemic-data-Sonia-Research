#  Sonia's Research - 
**An Analysis of the Spread and Transmission of COVID-19 in the United States Through Spatial Mobility Data Using a Network Model**

# Motivation
For the last year and a half I have been a Research Assistant for Dr. Philip Brown at the University of Colorado Colorado Springs writing Python code to explore and understand the spread and transmission of the COVID-19 virus in the United States. A few months ago, we began compiling all the work that I had done into a paper with the hopes that it will be published. This repository contains all of the Jupyter Notebooks and CSVs discussed in the report so that anyone can replicate both our research and our results.
<hr>

### What is our Research Question?
***How contagious is COVID-19? What are the beta values for COVID-19 over time?***
<hr>

### Methodology
Using an SEIR infectious disease model that accurately reflected the transmission and spread of COVID-19, we were able to derive equations for ${S(t+1), E(t), I(t+1), R(t+1), \beta(t)}$. In order to answer the research question above, each of the Jupyter Notebooks in this repository were used to build various data structures and CSV files, as well as compute values for each of these expressions. An in depth explanation of the methods I used as well as the derivation for each equation can be found in our paper.    
<hr>

### Results
The beta values for COVID-19 over a time span of 450 days, from January 17, 2020, to April 10, 2021, for all 3,133 U.S. counties can be found in this repository, under the “Data Jupyter 
Notebooks Build” subfolder, which is located in the “Data” folder. The file is titled beta_matrix.csv.
<hr>

### Contents of this Repository
Name of Folder/Subfolder | Contents of Folder/Subfolder
| :---: | --- 
<ins>Data</ins> Folder | contains 4 subfolders with all of the necessary data to run each Jupyter Notebook, examine our results, and read to avoid running code that takes a relatively long time to execute. 
<ins>A Matrices</ins> Subfolder | located in the <ins>Data</ins> Folder, contains  all 451 $\tilde{A}$ matrices for our model that are input to the ***Build Average A Matrix*** Jupyter Notebook
<ins>Aggregated A Matrix</ins> Subfolder | located in the <ins>Data</ins> Folder, contains the 3,133 rows by 451 columns Daily A Matrix that the ***Build Daily A Matrix*** Jupyter Notebook builds
<ins>Data Jupyter Notebooks Build</ins> Subfolder | located in the <ins>Data</ins> Folder, contains the CSV files that store the matrices for the population, case, and vaccine data, which can take a long time to build. This subfolder also contains the CSV containing all of the beta values the “Analysis with Network Models - Paper Notebook with Average A Matrix and New York City” Jupyter Notebook creates
<ins>Data Jupyter Notebooks Build</ins> Subfolder | located in the <ins>Data</ins> Folder, contains 5 CSVs that are input to Jupyter Notebooks
<ul><li>test1</li><li>test2</li></ul>
  1. Final_Paper_Data_avg_cases.csv – input to the ***Build A Matrices - with New York City*** Jupyter Notebook
  2. Test
<hr>


### Notes
***How contagious is COVID-19? What are the beta values for COVID-19 over time?***
<hr>
