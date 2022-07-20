# World Airplane Crashes Analysis(1908-2009)
### Cleaning and Analyzing data in Power query and Power BI

## Introduction
This project is my capstone project for [#30daysoflearning](https://techcommunity.microsoft.com/t5/educator-developer-blog/learning-data-analysis-curriculum-and-resources/ba-p/3497797) organized by [Olanrewaju Oyinbooke](https://github.com/theoyinbooke).
I analyzed a dataset from [kaggle](https://www.kaggle.com/datasets/saurograndi/airplane-crashes-since-1908) about airplane crashes and fatalities around the world from a period of 1908-2009.
The dataset contained 5268 cases of crashes and 13 columns which included information about date of crash,  number of people aboard, fatalities, location, its operator/airline,type of aircraft and a summary of the cause of the crash.

![Raw data](https://user-images.githubusercontent.com/61963973/179941566-2745fe26-fc19-4739-9d28-21967ba4b025.png)

## Data Cleaning 
After importing my data into power query, I checked for duplicates(found none),the validity of my data using column distribution, quality and profiling and removed columns not neccessary for my analysis.
I also made sure my columns were in the right data type.

![data cleaning](https://user-images.githubusercontent.com/61963973/179928540-19561e60-79c2-460b-8de6-4661b1e398c1.png)

## Data Preprocessing
I noticed the location column contained cities, states and countries so i split them using the "split by delimiter function"(since i needed the countries). In the newly created column, i discovered there were variations of spellings and USA was represented by its states. I cleaned this up using Fuzzy Clustering in Power query and replacing the states with country. You can find the power query scipt here.

![Data Processing](https://user-images.githubusercontent.com/61963973/179937153-e768d379-a1d4-4d4f-9fdc-c13742d57e8b.png)

To get the causes of crashes from the Summary column, I extracted the keywords from the column and used conditional column to group them into:
+ Mechanical Failure: invovling causes due to engine, propeller or wing failure.
+ Weather condition: includes crashes affected by any form of weather e.g rain, storm, fog etc.
+ Pilot error: involves loss of control.
+ Struck an Object: plane crashed into/or struck a mountain, tree etc.
+ Shot down: plane crashing due to being shot at
+ Fire Outbreak: plane crashed due to explosion or sudden fire.
+ Collision: airplanes colliding.
+ Fuel: crash caused by low fuel
+ Unknown causes

You can also find the scripts here.

![Data Processing 2](https://user-images.githubusercontent.com/61963973/179940972-75a93257-23c9-4ebc-a21d-3fb18621e6fc.png)

Lastly, I made a column to group each operator into  Civil or Military Aviation
Civil Aviation: this includes all aircrafts used for personla and business purposes rather than for military Purposes.
Military Aviation: this includes all aircfarts for the purposes of conducting or enabling warfare. 

 ## Data Analysis & Visualizations.
1. Crashes over the years: crashes kept increasing from 1908 as more aircrafts were produced and airlines came into the industry. In recent years there is a decrease in the crashes which can be drawn to technological advancements.
For Military Aviation, the highest year of crash was in 1945(marked the end of World War II).
2. Crashes over the months: December had the highest number of crashes followed after by January.
3. Aeroflot and The US Air force had the top most crashes. Aeroflot is Russia largest airline and one of the oldest airlines. Also, The US Airforce accounted for 22.54% of total Military aviation crashes.

![crash by airline](https://user-images.githubusercontent.com/61963973/179962355-3d7fb8cb-7180-41a9-bc81-7faec8d3acda.png)

4. The most Crashed aircraft was the Douglas DC 3. 

![type crash](https://user-images.githubusercontent.com/61963973/179962823-62d774b1-dd41-49c8-ab61-fdddbdf884f8.png)

5. 

