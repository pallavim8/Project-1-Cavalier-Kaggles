# Project-1-Cavalier-Kaggles

## Repository Overview

This repository contains all the code, data processing steps, exploratory analysis, and results for our project. The project examines how sentiment expressed in Yelp text reviews compares to numerical star ratings. The goal of the project is to identify and analyze consistent mismatches between text-based sentiment and ratings across different restaurant cuisines using data analysis and statistical testing.

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
- nltk
- re
- vaderSentiment

All packages can be installed via `pip` if they are not already available.

### Platform
- Developed and tested on macOS  
- Expected to run on Windows and Linux without modification  

## Map of the Repository

Below is an outline of the repository structure and its contents:

project-root/
│
├── data/
│ ├── raw/ # Original, unmodified dataset(s)
│ └── processed/ # Cleaned and filtered data used for analysis
│
├── notebooks/
│ ├── 01_data_cleaning.ipynb
│ ├── 02_exploratory_analysis.ipynb
│ └── 03_statistical_analysis.ipynb
│
├── results/
│ ├── figures/ # Saved plots and visualizations
│ └── tables/ # Summary tables and statistical outputs
│
├── README.md # Project overview and reproduction instructions
└── requirements.txt # List of required Python packages


## Instructions for Reproducing Results

Run the DS 4002 Project 1 Jupyter Notebook in Google Colab

