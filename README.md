#  Sonia's Research - 
**An Analysis of the Spread and Transmission of COVID-19 in the United States Through Spatial Mobility Data Using a Network Model**

# Motivation
For the last year and a half I have been a Research Assistant for Dr. Philip Brown at the University of Colorado Colorado Springs writing Python code to explore and understand the spread and transmission of the COVID-19 virus in the United States. A few months ago, we began compiling all the work that I had done into a paper with the hopes that it will be published. This repository contains all of the Jupyter Notebooks and CSVs discussed in the report so that anyone can replicate both our research and our results.
<hr>

### What was our Research Question?
***How contagious is COVID-19? What are the beta values for COVID-19 over time?***
<hr>

### Methodology
Using an SEIR infectious disease model that accurately reflected the transmission and spread of COVID-19, we were able to derive equations for ${S(t+1), E(t), I(t+1), R(t+1)}$ and ${\beta(t)}$. In order to answer the research question above, each of the Jupyter Notebooks in this repository were used to build various data structures and CSV files, as well as compute values for each of these expressions. An in-depth explanation of the methods I used as well as the derivation for each equation can be found in our paper.    
<hr>

### Results
The beta values for COVID-19 over a time span of 450 days, from January 17, 2020, to April 10, 2021, for all 3,133 U.S. counties can be found in this repository, under the <ins>Data Jupyter Notebooks Build</ins> subfolder, which is located in the <ins>Data</ins> folder. The file is titled beta_matrix.csv.
<hr>

### Contents of this Repository
Name of Folder/Subfolder or file | Contents of Folder/Subfolder or file
| :---: | --- 
|<ins>Data</ins> Folder | contains 4 subfolders with all of the necessary data to run each Jupyter Notebook, examine our results, and read to avoid running code that takes a relatively long time to execute. 
|<ins>A Matrices</ins> Subfolder | located in the <ins>Data</ins> Folder, contains  all 451 $\tilde{A}^T$ matrices for our model that are input to the ***Build Average A Matrix*** Jupyter Notebook
|<ins>Aggregated A Matrix</ins> Subfolder | located in the <ins>Data</ins> Folder, contains the 3,133 rows by 451 columns Daily A Matrix that the ***Build Daily A Matrix*** Jupyter Notebook builds
|<ins>Data Jupyter Notebooks Build</ins> Subfolder | located in the <ins>Data</ins> Folder, contains the CSV files that store the matrices for the population, case, and vaccine data, which can take a long time to build. This subfolder also contains the CSV containing all of the beta values the ***Analysis with Network Models - Paper Notebook with Average A Matrix and New York City*** Jupyter Notebook creates
|<ins>Jupyter Notebook input</ins> Subfolder | located in the <ins>Data</ins> Folder, contains 5 CSVs that are input to Jupyter Notebooks
|<ins>Jupyter Notebooks</ins> Folder | contains all of the necessary Notebooks to recreate our study
|<ins>beta_vs_sum_of_mobility_scatter_plot_data</ins> Folder | contains the data for the Beta vs. Sum of Mobility scatter plots. This folder contains CSVs for 7 counties: Orange County, CA, San Francisco County, CA, Denver County, CO, El Paso County, CO, Hudson County, NJ, New York City County, NY and Perry County, PA.
|<ins>environment.yml </ins> File | this file can be used to replicate the conda environment that I used to write all of the Jupyter Notebooks included in this repository

Below shows which Jupyter Notebook each CSV in the <ins>Jupyter Notebook input</ins> Subfolder uses as input - 
 1. Final_Paper_Data_avg_cases.csv – input to the ***Build A Matrices - with New York City*** Jupyter Notebook
 2. Final_Paper_Data_avg_cases_with_New_York_City.csv – input to the ***Analysis with Network Models - Paper Notebook with       Average A Matrix and New York City*** Jupyter Notebook
 3. Paper_Data_avg_cases_with_New_York_City.csv – input to the ***Build Paper CSV - with New York City*** Jupyter Notebook
 4. RegionsDashboard.csv – input to the ***Automate Data (Create a CSV File) – New York Times Rolling-Averages*** Jupyter Notebook
 5.covid_county_population_usafacts.csv – input to the ***Build Paper CSV - with New York City*** Jupyter Notebook 
<hr>

### Notes
- Due to file size, the CSVs for the vaccine data and Average A Matrix could not be uploaded to this 
repository. Nonetheless, the vaccine data CSV can be downloaded from the URL listed below while the Average A Matrix can be built using the Jupyter Notebook titled ***Build Average A Matrix***. The vaccine data CSV is required as input for the Notebook called ***Automate Data (Create a CSV File) – New York Times Rolling-Averages***, while the CSV containing the Average A matrix is required as input for the ***Analysis with Network Models - Paper Notebook with Average A Matrix and New York City*** Jupyter Notebook in order to calculate the beta values.
      The vaccine data is in a file called COVID-19_Vaccinations_in_the_United_States_County.csv and can be located and downloaded at the URL below. 
          
          URL: https://data.cdc.gov/Vaccinations/COVID-19-Vaccinations-in-the-United-States-County/8xkx-amqh
          
- The cells of the ***Analysis with Network Models - Paper Notebook with Average A Matrix and New York 
City*** Jupyter Notebook that builds the structures containing the case, vaccine, population, and beta
values data can take some time to execute. Due to this, at the very beginning of the notebook exists a 
flag called run_flag that is initially set to False. When this flag is set to True, the code that creates these 
structures will execute. On the other hand, when this flag variable is set to False, this code will 
not execute. Rather, these structures will be built by reading in the data from the CSVs that are already 
created, which are all located in the <ins>Data</ins> folder under the <ins>Data Jupyter Notebooks Build</ins> subfolder.

- At the very top of each Jupyter Notebook are path variables that can be set for input and output files. The default path is the file path in this GitHub repository. This allows the user to clone this repository and replicate our results. 
<hr>
