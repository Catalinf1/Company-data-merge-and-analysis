# Company Data Merger and Analysis

This repository contains a Jupyter notebook that demonstrates the process of merging and analyzing company data from multiple sources using PySpark.

## Table of Contents

- Overview
- Requirements
- Dataset
- Key Features
- Installation
- Usage
- Results
- Contributing
- License

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
2. Install the required packages:

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
