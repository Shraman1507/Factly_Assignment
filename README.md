# Factly Assignment Scripts

## Overview

This repository contains three Python scripts designed for various data processing tasks including web scraping, data cleaning, and transformation. Each script performs specific operations on educational data from the Ministry of Education's website.

## Repository Structure


Factly_assignment/
│
├── Scrape_files.py
├── Cleaning_14_15.py
├── Cleaning_15_16.py
├── README.md
└── data/
    └── AISHE2014-15.xlsx
    └── AISHE2015-16.xlsx


## Prerequisites

Ensure you have the following Python libraries installed:

- `requests`
- `beautifulsoup4`
- `html5lib`
- `pandas`
- `openpyxl`

You can install these dependencies using pip:


pip install requests beautifulsoup4 html5lib pandas openpyxl

## Setup Instructions

1. **Clone the Repository:**


   git clone https://github.com/yourusername/Factly_assignment.git
   cd Factly_assignment
   

2. **Ensure Data Files are Present:**

   Place the `AISHE2014-15.xlsx` and `AISHE2015-16.xlsx` files in the `data/` directory.

## Script 1: Scrape_files

### Description

This script fetches PDF and Excel files from the Ministry of Education's website, navigating through multiple pages to download all relevant files.

### Usage

1. **Setup Constants:**
   - URL of the main page to scrape.
   - Headers for the HTTP requests.
   - Base URL and output directory.

2. **Run the Script:**

   
   python Scrape_files.py


### Functionality

- **Fetch and Parse Main Page:**
   The script fetches the content of the main page and parses it using BeautifulSoup.

- **Extract and Download URLs:**
   It extracts URLs of PDF and Excel files and downloads them to the specified directory.

- **Handle Pagination:**
   It checks for a link to the next page, fetches it, and processes the next page similarly.

## Script 2: CLeaning_15_16

### Description

This script processes an Excel file (`AISHE2015-16.xlsx`). It reads data from the '6TotalEnr' sheet, standardizes column names, reshapes the data, and saves it to a new Excel file.

### Usage

1. **Run the Script:**

   
   python Cleaning_15_16.py
   


### Remainder:
- Enter the file location of AISHE2014-15 excel sheet accordingly in "pd.read_excel"
  
### Functionality

- **Load Excel File:**
   Load the Excel file and select the relevant sheet and headers.

- **Standardize Column Names:**
   Standardize column names to ensure consistency and clarity.

- **Reshape Data:**
   Reshape the DataFrame using `pd.melt`.

- **Save Processed Data:**
   Add additional columns, fill empty cells with `np.nan`, and save the processed DataFrame to a new Excel file (`AISHE2015_16_processed.xlsx`).

## Script 3: Cleaning_14_!5

### Description

This script processes an Excel file (`AISHE2014-15.xlsx`). It reads data from the '1UniNo' sheet, standardizes column names, reshapes the data, and saves it to a new Excel file.

### Usage

1. **Run the Script:**

   
   python Process_AISHE2014_15.py
   
### Remainder:
- Enter the file location of AISHE2014-15 excel sheet accordingly in "pd.read_excel"

### Functionality

- **Load Excel File:**
   Load the Excel file and select the relevant sheet and headers.

- **Standardize Column Names:**
   Standardize column names to ensure consistency and clarity.

- **Reshape Data:**
   Reshape the DataFrame using `pd.melt`.

- **Save Processed Data:**
   Add additional columns, fill empty cells with `np.nan`, and save the processed DataFrame to a new Excel file (`AISHE2014_15_processed.xlsx`).

## Conclusion

These scripts are designed to automate the process of downloading, cleaning, and reshaping educational data from Excel files. They ensure consistency in column names and structure, making the data easier to analyze and use for further tasks.

---

This README provides a comprehensive guide for anyone who wants to understand and run the scripts in your repository.
