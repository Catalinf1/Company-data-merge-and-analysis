# Company Data Merger and Analysis

This repository contains a Jupyter notebook that demonstrates the process of merging and analyzing company data from multiple sources using PySpark.

## Table of Contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Dataset](#dataset)
- [Key Features](#key-features)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Approach and Methodology](#approach-and-methodology)

## Overview
This project showcases the use of PySpark to merge and analyze company data from three different sources: Facebook, Google, and company websites. The notebook covers data loading, preprocessing, merging, conflict resolution, and analysis, providing insights into the geographical and categorical distribution of companies.

## Requirements

- Python 3.10+
- PySpark
- Pandas
- Matplotlib
- Seaborn

## Dataset
The project uses three datasets:

```facebook_dataset.csv```

```google_dataset.csv```

```website_dataset.csv```

These datasets contain information about companies, including their names, addresses, categories, and contact information.
## Key Features

- Data loading and preprocessing using PySpark
- Merging of datasets from multiple sources
- Conflict resolution for inconsistent data
- Data quality checks and imputation of missing values
- Analysis of company distribution by country and category
- Visualization of key insights

## Installation

1. Clone this repository:
   
   `git clone https://github.com/yourusername/company-data-merger.git`
   
3. Install the required packages:

   `pip install pyspark pandas matplotlib seaborn`

## Usage

1. Open the Jupyter notebook `Datasets join.ipynb` in your preferred environment (e.g., Jupyter Lab, Kaggle, VS Code).
2. Run the cells in order to execute the data processing and analysis pipeline.
3. The final merged dataset will be saved as `merged_company_data.csv` in the working directory.

## Results

The notebook provides several insights, including:

- Distribution of companies across countries
- Most common company categories
- Analysis of companies with multiple phone numbers
- Completeness of data (missing values analysis)
- Distribution of domain TLDs

A bar plot visualizing the top 10 countries by number of companies is also generated.

## Approach and Methodology

### Project Context and Relevance

This project is highly relevant to the recruitment process as it demonstrates the ability to handle and merge large datasets from multiple sources, a key skill in data engineering and analysis. It relates directly to Veridion's work in gathering and processing business data from various sources to provide comprehensive company information.

The outcome of this project can create significant business value by:
1. Enhancing the quality and completeness of company data
2. Providing insights into data distribution and quality across different sources
3. Establishing a robust methodology for data merging and conflict resolution

### Data Investigation

I approached the data investigation phase with the following steps:
1. Loading each dataset and examining its schema
2. Performing basic statistical analysis (count, distinct values, null values)
3. Analyzing the distribution of key fields like country, category, and domain

This investigation helped in understanding the structure and quality of each dataset, guiding the subsequent cleaning and merging processes.

### Data Cleaning

The data cleaning process involved:
1. Standardizing column names across datasets
2. Handling missing values through imputation where appropriate
3. Standardizing country names and codes
4. Cleaning and formatting phone numbers
5. Validating data types and formats (e.g., ensuring valid country codes)

### Data Join Reasoning

1. Join Column: I chose to use the 'domain' column as the primary join key. This decision was based on the assumption that a company's domain is likely to be unique and consistent across different data sources.

2. Data Conflicts: In cases of conflicting data, I implemented a priority system:
   Website data > Google data > Facebook data
   This hierarchy was chosen based on the assumption that a company's own website is likely to have the most up-to-date information.

3. Similar Data: For very similar data, I kept the most complete and recent information. In cases where it wasn't clear which was more recent, I defaulted to the priority system mentioned above.

4. Final Dataset: The final dataset includes all non-conflicting information from all three sources. This approach maximizes the completeness of our company profiles while maintaining data integrity.



