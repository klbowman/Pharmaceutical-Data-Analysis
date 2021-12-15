# Data Visualization with Matplotlib

Data cleaning, analysis, and visualization for a pharmaceutical testing laboratory.

## Description

This repository is designed to analyze laboratory test results from a study aimed at developing treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. 

Sample metadata and study results are stored in 2 CSV files (Mouse_metadata.csv, Study_results.csv) in the **data** directory of Pymaceuticals. These files are imported into Jupyter Notebook (pymaceuticals_kbowman.ipynb) and merged using a left join. Duplicate mouse IDs are dropped before calculating summary statistics (mean, standard deviation, median, variance, standard error of the mean) for each drug regimen tested in the study. 

Data is visulaized using Pandas and Matplotlib to create the following: 
- Bar plot showing the total number of timepoints for all mice tested for each drug regimen.
- Pie plot that shows the distribution of female or male mice in the study.


The dashboard includes a drop-down menu that displays the numerical code for each individual sample. When a sample is selected, the “Demographic Info” panel is populated with metadata and the following three charts are populated with data:
* Bar graph displaying the top 10 OTUs by count
* Gauge plot showing the belly button scrubs per week
* Bubble plot displaying OTU counts for the entire sample

<p align="center">
  <img src="https://user-images.githubusercontent.com/74067302/145615550-98e49162-44c9-4e39-9050-ba837dc42863.png" alt="Dashboard Image"/>
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/74067302/145615561-5fc19f35-646b-47aa-9f63-4a93a495efe5.png" alt="Dashboard Image"/>
</p>

## Getting Started

### Technologies Used 

* Jupyter Notebook
* Python
* Pandas
* Matplotlib

### Installing

* Clone this repository to your desktop.
* Navitage to the home directory and open index.html in your browser.

### Data Sources

* Hulcr J, Latimer AM, Henley JB, Rountree NR, Fierer N, et al. (2012) A Jungle in There: Bacteria in Belly Buttons are Highly Diverse, but Predictable. PLoS ONE 7(11): e47712. doi:10.1371/journal.pone.0047712 [Access Data](http://robdunnlab.com/projects/belly-button-biodiversity/results-and-data/)


## Authors

Katlin Bowman, PhD

E: klbowman@ucsc.edu

[LinkedIn](https://www.linkedin.com/in/katlin-bowman/)
