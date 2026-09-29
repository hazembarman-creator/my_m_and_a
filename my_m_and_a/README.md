# Welcome to My M And A
***

## Task
We recently acquired a new company (Only Wood Box) that has its own customer databases spread across three CSV files, all in heterogeneous and poorly standardized formats. The challenge is to merge these three data sources, clean and harmonize the columns, and then integrate everything into our single, robust customer database (Plastic Free Boutique).

The challenge lies in:

Cleaning the data (different columns, combined fields, stray characters)

Harmonizing the schema to match our structure

Managing the pipeline so that no .csv files remain in the repository using .gitignore file


We recently acquired a new company (Only Wood Box) that has its own customer databases spread across three CSV files, all in heterogeneous and poorly standardized formats. The challenge is to merge these three data sources, clean and harmonize the columns, and then integrate everything into our single, robust customer database (Plastic Free Boutique).

The challenge lies in:

Cleaning the data (different columns, combined fields, stray characters)

Harmonizing the schema to match our structure

Managing the pipeline so that no .csv files remain in the repository using .gitignore file



## Description
The my_m_and_a function performs a comprehensive ETL (Extract, Transform, Load) process:

Data Extraction:
Accepts three CSV file contents as input (either string content or StringIO objects)

Uses pandas to load each CSV into separate DataFrames

Handles different file formats including standard CSV, semi-colon delimited, and complex tab-separated formats

Data Transformation & Cleaning:
Database 1: Standard CSV format with column normalization and removal of unnecessary columns like 'username'

Database 2: Semi-colon delimited data requiring header reconstruction, name field parsing, and special character removal

Database 3: Complex tab-separated format with embedded prefixes that require extraction and normalization

Schema Harmonization:
Standardizes all columns to PascalCase format: Gender, FirstName, LastName, Email, Age, City, Country, Created_At, Referral

Gender Normalization: Converts various formats (M/F/1/0) to standardized 'Male'/'Female' values

Name Cleaning: Removes "string_" prefixes, special characters, and properly splits combined name fields

Age Handling: Converts all age values to strings with proper null value management

City Formatting: Ensures all city names are in proper title case format

Data Validation: Guarantees all required columns are present with appropriate data types

Data Integration:
Merges the three cleaned DataFrames into a single unified dataset

Maintains data integrity throughout the merging process

Returns the final DataFrame for validation and testing purposes

Database Integration:
Converts the final DataFrame to CSV format

Calls the csv_to_sql function from my_ds_babel to insert data into the SQLite database

Ensures seamless migration to the Plastic Free Boutique customer database

## Installation
Clone the project.
git clone git@git.us.qwasar.io:my_m_and_a_186993_amburg/my_m_and_a.git
git cd my_m_and_a
Create a Python environment (>=3.8 recommended).
Install pandas:
pip install pandas
Check that the internal dependencies (my_ds_babel.py) are present.

Add your CSV files to .gitignore to comply with the guidelines:

Copy code *.csv


Clone the project.
git clone git@git.us.qwasar.io:my_m_and_a_186993_amburg/my_m_and_a.git
git cd my_m_and_a
Create a Python environment (>=3.8 recommended).
Install pandas:
pip install pandas
Check that the internal dependencies (my_ds_babel.py) are present.

Add your CSV files to .gitignore to comply with the guidelines:

Copy code *.csv

## Usage
Prepare your CSV files:
Place your three CSV files in the project directory
Add the paths of your csv files in the 3 different variables located in your main function
Run the code:

 python my_m_and_a.py
Output:
Cleaned and merged customer data in SQL database

DataFrame returned

Comprehensive data quality assurance through the transformation process

Prepare your CSV files:
Place your three CSV files in the project directory
Add the paths of your csv files in the 3 different variables located in your main function
Run the code:

 python my_m_and_a.py
Output:
Cleaned and merged customer data in SQL database

DataFrame returned

Comprehensive data quality assurance through the transformation process
```
./my_project argument1 argument2
```

### The Core Team


<span><i>Made at <a href='https://qwasar.io'>Qwasar SV -- Software Engineering School</a></i></span>
<span><img alt='Qwasar SV -- Software Engineering School's Logo' src='https://storage.googleapis.com/qwasar-public/qwasar-logo_50x50.png' width='20px' /></span>
