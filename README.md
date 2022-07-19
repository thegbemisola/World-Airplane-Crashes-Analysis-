# World Airplane Crashes Analysis(1908-2009)
Cleaning and Analyzing data in Power query and Power BI

## Introduction
This project is my capstone project for [#30daysoflearning](https://techcommunity.microsoft.com/t5/educator-developer-blog/learning-data-analysis-curriculum-and-resources/ba-p/3497797) organized by [Olanrewaju Oyinbooke](https://github.com/theoyinbooke).
I analyzed a dataset from [kaggle](https://www.kaggle.com/datasets/saurograndi/airplane-crashes-since-1908) about airplane crashes and fatalities around the world from a period of 1908-2009.
The dataset contained 5268 cases of crashes and 13 columns which included information about date of crash,  number of people abroad, fatalities, location and its operator/airline,type of aircraft and a summmary of the cause of the crash.

## Data Cleaning 
After importing my data into power query I checked for duplicates(found none),the validity of my data using column distribution, quality and profiling and removed columns not neccessary for my analysis.
I also made sure my columns were in the right data type.

## Data Preprocessing
I noticed the location columns contained cities, states and countries so i split them using the "split by delimiter function"(since i needed the countries). In the newly created column, i discovered there were variations of spellings and USA was represented by its states. I cleaned this up using Fuzzy Clustering in Power query and replacing the states with country. You can find the power query scipt here.

To get the causes of crashes from my Summary column, I had to 
