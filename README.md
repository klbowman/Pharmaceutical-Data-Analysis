# Data Visualization with Matplotlib

Data cleaning, analysis, and visualization for a pharmaceutical testing laboratory.

## Description

This repository is designed to analyze laboratory test results from a study aimed at developing treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. 

Sample metadata and study results are stored in 2 CSV files (Mouse_metadata.csv, Study_results.csv) in the **data** directory of Pymaceuticals. These files are imported into Jupyter Notebook (pymaceuticals_kbowman.ipynb) and merged using a left join. Duplicate mouse IDs are dropped before calculating summary statistics (mean, standard deviation, median, variance, standard error of the mean) for each drug regimen tested in the study. 

Data is visualized using Pandas and Matplotlib to create the following: 
- **Bar plot** showing the total number of timepoints for all mice tested for each drug regimen.
- **Pie plot** that shows the distribution of female or male mice in the study.
<p align="center">
  <img src="https://user-images.githubusercontent.com/74067302/146280272-0b611c21-0dc3-44d2-8edb-80daffae1b15.png" alt = "Bar plot" width="500" />
  <img src="https://user-images.githubusercontent.com/74067302/146280283-4998249e-3d50-47de-8e88-1c7bb6f79dd9.png" alt = "Pie chart"width="300" /> 
</p>

The final tumor volume of each mouse across four of the most promising treatment regimens (Capomulin, Ramicane, Infubinol, and Ceftamin) is calculated using Pandas GroupBy and loc functions, then quartiles and IQR are used to quantitatively determine if there are any potential outliers across all four treatment regimens. After outliers are removed, a **box plot** of the final tumor volume of each mouse across four regimens of interest is created using Matplotlib.
<p align="center">
  <img src="https://user-images.githubusercontent.com/74067302/146280988-4fa5b4e9-f5b2-4b03-a4eb-c1f03e789058.png" alt = "Box plot"/>
</p>

A **scatter plot** of tumor volume versus mouse weight for the Capomulin treatment regimen is created, and data for mouse #185 (treated with Capomulin) is used to generate a **line plot** of tumor volume vs. time. The correlation coefficient and linear regression model are determined for the scatterplot of mouse weight and average tumor volume for the Capomulin treatment using scipy.stats. Finally, the **linear regression model** is plotted on top of the previous scatter plot.
<p align="center">
  <img src="https://user-images.githubusercontent.com/74067302/146281207-d0bdce17-eb0d-4231-885b-e94a01ef8232.png" width="400" alt="Line plot" />
  <img src="https://user-images.githubusercontent.com/74067302/146282055-cc16d122-4b5c-4e84-b294-589754337b0e.png" width="500" alt = "Scatter plot" /> 
</p>

## Getting Started

### Technologies Used 

* Jupyter Notebook
* Python
* Pandas
* Matplotlib
* NumPy
* scipy.stats

### Installing

* Clone this repository to your desktop.
* Navigate to the Pymaceuticals directory and run the pymaceuticals_kbowman.ipynb file in Jupyter Notebook.

### Data Sources

* Mockaroo, LLC. (2021). Realistic Data Generator. https://www.mockaroo.com/

## Author

Katlin Bowman, PhD

E: klbowman@ucsc.edu

[LinkedIn](https://www.linkedin.com/in/katlin-bowman/)
