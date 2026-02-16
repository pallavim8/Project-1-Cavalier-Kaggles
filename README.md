# Project-1-Cavalier-Kaggles

## Repository Overview

This repository contains all the code, data processing steps, exploratory analysis, and results for our project. The project examines how sentiment expressed in Yelp text reviews compares to corresponding numerical star ratings. The goal of the project is to identify and analyze consistent mismatches between text-based sentiment and corresponding star ratings across different restaurant cuisines using data analysis and statistical testing.

## Software and Platform

### Software
- Python3  
- Jupyter Notebook  

### Required Packages
The following Python packages are required to run the notebooks:
- pandas  
- numpy  
- matplotlib  
- langdetect
- googletrans-py
- vaderSentiment

All packages can be installed via `pip` if they are not already available.

### Platform
- Developed and tested on macOS  
- Expected to run on Windows and Linux without modification  

## Map of the Repository
Below is an outline of the repository structure and its contents:

<pre><code>project-root/
├─ SCRIPTS/
│  ├─ DS_4002_Project_1.ipynb
├─ DATA/
│  └─ yelp_academic_dataset_review.json
│  └─ yelp_academic_dataset_business.json
│  └─ final_dataset.csv
├─ OUTPUT/
│  └─ figures/
│  └─ tables/
│  └─ process/
├─ README.md
└─ LICENSE.md
</code></pre>

## Instructions for Reproducing Results

To reproduce the results of our project, please run each cell in the DS 4002 Project 1 Jupyter Notebook (i.e. DS_4002_Project_1.ipynb) on a Google Colab Python3 runtime in the order indicated within the file.

In the event the provided Jupyter Notebook fails to run, take the following steps to reproduce our results:
  1. Load yelp_academic_dataset_review.json (first 200,000 records only) and yelp_academic_dataset_business.json into the runtime as DataFrames.
  2. Filter the business data set to include only records with “Restaurant” present in the categories column.
  3. Inner join the data sets on the business_id columns.
  4. For each record in the merged data set, create a cuisine column which contains all values in the categories column for that record found in the following list:
     American, Mexican, Italian, Chinese, Japanese, Thai, Vietnamese, Korean, Mediterranean, Greek, French,   Spanish, Breakfast, Brunch, Pizza, Burgers, Seafood, BBQ, Sushi, Ramen, Cafes, Coffee, Bakeries, Desserts, Fast Food, Vegetarian, Vegan, Halal, Kosher
  6. Translate any non-English review text.
  7. Drop any empty records or any records without a value in the cuisine column.
  8. Scale the star ratings for each record to a min-max range of 0-1. 
  9. Generate a composite sentiment score for each record using the vaderSentiment package on the review text in English.
  10. For each record, store the difference of the sentiment score and the scaled star rating in the direction column and the absolute value of the direction column in the mismatch column.
  11. For each record, explode the data set so that new records are created for each value in the cuisine column.
  12. Run an ANOVA using the cuisine column as the categories and the mismatch column as the values.
  13. Repeat steps 1 through 9. For each record with multiple values in the cuisine column, pick one value to keep at random. Repeat step 11.

Note: final_dataset.csv is reference only and does not functionly replace either yelp_academic_dataset_review.json or yelp_academic_dataset_business.json in the provided notebook.

