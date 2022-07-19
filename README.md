# World Airplane Crashes Analysis(1908-2009)
Cleaning and Analyzing data in Power query and Power BI

## Introduction
This project is my capstone project for #30daysoflearning organized by [Olanrewaju Oyinbooke](https://github.com/theoyinbooke).
I analyzed a dataset from [kaggle](https://www.kaggle.com/datasets/saurograndi/airplane-crashes-since-1908) about airplane crashes and fatalities around the world from a period of 1908-2009.
The dataset contained 5248 cases of crash with information about when it occurred, number of people abroad, fatalities, location and its operator/airline.

## Data Cleaning 
I imported my data into power query in excel. Then I checked for duplicates. Also used column distribution, quality and profiling to understand the validity of the data. I removed columns not neccessary for my analysis.
I also made sure my columns were in the right data type.
## Data Preprocessing
I noticed the location columns contained cities, states and countries so i split them using the "split by delimiter function"(since i needed the countries). in the newly created column, i discovered there were variations of spellings and USA was represented by its states. I cleaned this up using Fuzzy Clustering in Power query and replacing the states with country. You can find the power query scipt here.

To get the causes of crashes from my Summary column, 
