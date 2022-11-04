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
    |- RAW_us_confirmed_cases.csv
    |- mask-use-by-county.csv
    |- U.S._State_and_Territorial_Public_Mask_Mandates_From_April_10__2020_through_August_15__2021_by_County_by_Day.zip
  |- Part 1- Jupyter notebook.ipynb
  |- Part 1- Collective Analysis - Reflection Statement.pdf
  |- Part 1- Collective Analysis - Visualization Explanation.pfd
  |- Visualization.png
```

## Input files 

1) RAW_us_confirmed_cases.csv : The RAW_us_confirmed_cases.csv file from the Kaggle repository of [John Hopkins University COVID-19 data](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university). This data is updated daily. You can use any revision of this dataset posted after October 1, 2022.
2) mask-use-by-county.csv : The New York Times [mask compliance survey](https://github.com/nytimes/covid-19-data/tree/master/mask-use) data.
3) U.S._State_and_Territorial_Public_Mask_Mandates_From_April_10__2020_through_August_15__2021_by_County_by_Day.zip : The CDC dataset of [masking mandates by county](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i). Note that the CDC stopped collecting this policy information in September 2021.

[Pageviews API](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews)

## Jupyter Notebook
Part 1- Jupyter notebook.ipynb : Contains the code used for analysis and plotting the visualization

## Outputs/Visualizations Obtained
1) Part 1- Collective Analysis - Reflection Statement.pdf : Provides a reflection statement on what I got out of this collaborative assignment
2) Part 1- Collective Analysis - Visualization Explanation.pfd : Provides an explanation of the visualization obtained
3) Visualization.png - Display the final visualization obtained

## Issues/ Special considerations
1) Moving average (over 7 days) of the daily cases counts data also incorporated in the analaysis and visualization approach to account for case counts not being updated for every single day in a week to help smooth out-trend information by creating a constantly updated average value in the visualization.
2) Apart from the CDC masking mandate data, Jefferson County's official website stating the masking policies have also been considered in the output visualization.


## Snapshot of visual analysis
![Visualization](/Visualization.png)

Above is a time series plot visualizing the variations in the COVID-19 daily infection rate in Jefferson County (state of Kentucky) during and beyond the periods when mask mandate policies were established in Jefferson County.

1)	Here, the X-axis represents the dates for which the cumulative inflected case count is made available through the RAW_us_confirmed_cases.csv data set for Jefferson County. The Y-axis represents the number of cases per day which is derived by subtracting the previous date's cumulative inflected case count from the current date's cumulative inflected case count.
2) The changepoints (represented by the red dotted lines) indicate the abrupt variations in the rate of infections i.e., timestamps where the change in inflected cases is significant from the confirmed cases dataset made available for Jefferson County. These changepoints were calculated using Pruned Exact Linear Time (PELT) Test
3) The mask mandate policies data w.r.t Jefferson County is also incorporated into this visual. The 2 black dotted lines represent the date boundary for which mask mandate policy information is available in the US State and Territorial Public Mask mandates data provided (ie., from 04/10/2020 to 08/15/2021) The green line within this date boundary represents the variations in the daily infection rate when mandatory mask usage was established in Jefferson County and the blue line within this date boundary represents the variations in the daily infection rate when mandatory mask usage was not established in Jefferson County. The blue line beyond the date boundary represents the variations in the daily infection rate during periods where there is no information regarding the mask mandate policy in Jefferson County.
4)The continuous black line depicted over all dates in the x-axis indicates the 7-day moving average of the daily case rate. This is to account for case counts not being updated for every single day in a week and it helps smooth out-trend information by creating constantly updated average rates.

## Observations/Inferences: 

Through this visual, we can see that the masks were made mandatory from mid-June 2020 to mid-July 2021 (7/10/2020 to 6/10/2021) in Jefferson County. It is interesting to see that before and during the start of the mask mandate, we see that cases per day spread was kind of controlled and during the central period (Oct 2020 to Feb 2021) of the mask mandate the spread seems to move towards an uncontrolled trend. However, the same cannot be said during the end of the mask mandate. We see a controlled spread during the beginning of the end of the mask mandate period (i.e., from Mar 2021 to June 2021). If we were to consider the masking mandate to be the sole reason for the trend period, one can say the effects of removing the mask mandate can be observed in a little over the next 30 days’ time period (i.e., from Aug 2021) were the cases per day are starting to spread uncontrolled again. The voluntary masking survey shows us that 60.2% of the people in this county always wore masks and 91.5% of people wore masks more than sometimes (including sometimes survey points). This timeframe (July 2 - July 14) was when CDC had nationwide guidelines for wearing masks. So, technically our assumption is people in the county were following CDC guidelines religiously when there was a state mandate. Hence, these non-uniform variations in the case rates during different mask mandate periods lead me to infer that perhaps the mask mandates are not the only factor impacting the case rate variations. Additionally, moving away from the impact of mask mandates, we see that there is a huge uncontrolled spike in the case rates for Jefferson County at the beginning of the year 2022. One explanation for this can be the rise of the Omicron variant detection in several counties of the United States at the beginning of 2022.


## Author
- [Shubha Changappa Palachanda](https://github.com/shubha8196)
