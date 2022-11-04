[![license](https://img.shields.io/github/license/DAVFoundation/captain-n3m0.svg?style=flat-square)](https://github.com/DAVFoundation/captain-n3m0/blob/master/LICENSE)
![contributors](https://img.shields.io/github/contributors/shubha8196/data-512-homework_1.svg) ![codesize](https://img.shields.io/github/languages/code-size/shubha8196/data-512-homework_1.svg)


# data-512-part1_common_analysis: Part1- Common Analysis

This repository contains all the required materials for Part 1 of the DATA 512 course project. DATA 512 is the Human Centered Data Science course (Autumn 2022) offered by the MSDS program at the University of Washington. 

## Goal

For the past three years, we have all been afflicted by a global epidemic. One element that has been difficult to overlook over the last three years is the datafication of the pandemic. In other words, a large amount of information about the human cost of the epidemic has been acquired, compiled, and presented as statistics. We may analyze the pandemic from a number of perspectives with the use of this data in order to understand how it has impacted as well as society. To be frank, we are just now beginning to comprehend and appreciate their consequences. We hope to look at some of the social components of the pandemic during this course project by completing a human-centered data science assessment of the current COVID-19 data. Part 1: Common Analysis will be used by all students throughout the course. Students will be tasked with assessing data for a specific US county.

County Assigned: Jefferson County, Kentucky, United States

## Data Utilized
The data extracted for this project has different aspects and way of collection. One source is CDC for county specific information, other John Hopkins with confirmed cases data shared on Kaggle and other is New York Times Survey data.

Dataset Sources
The RAW_us_confirmed_cases.csv file from the Kaggle repository of John Hopkins University COVID-19 data. This data is updated daily and recent version is used
The CDC dataset of masking mandates by county. Note that the CDC stopped collecting this policy information in September 2021.
The New York Times mask compliance survey data.


## Repository Distribution

```
data-512-homework_1/
  |- README.md
  |- LICENSE
  |- data
    |-
    |-
    |-
  |- Part 1- Jupyter notebook.ipynb
  |- Part 1- Collective Analysis - Reflection Statement.pdf
  |- Part 1- Collective Analysis - Visualization Explanation.pfd
  |- Visualization.png
```
##Input files 

## Jupyter Notebook
Part 1- Jupyter notebook.ipynb : Contains the code used for analysis and plotting the visualization

## Outputs/Visualizations Obtained
 Part 1- Collective Analysis - Reflection Statement.pdf
 Part 1- Collective Analysis - Visualization Explanation.pfd
 Visualization.png

## Issues/ Special considerations
1) Moving average (over 7 days) of the daily cases counts data also incorporated in the analaysis and visualization approach to account for case counts not being updated for every single day in a week to help smooth out-trend information by creating a constantly updated average value in the visualization.
2) Apart from the CDC masking mandate data, Jefferson County's official website stating the masking policies have also been considered in the output visualization.

## Author
- [Shubha Changappa Palachanda](https://github.com/shubha8196)
