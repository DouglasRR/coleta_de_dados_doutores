# Data Collection from Gynecologists in MG (Doctoralia)

## Goal

This code is a solution for collecting data from all gynecologists in Belo Horizonte, MG, from the Doctoralia website. It extracts information such as city, name, phone and link from each gynecologist profile.

## Functionality

The code uses the BeautifulSoup library to perform web scraping and collect data from gynecologist profiles. It starts by visiting each search results page on the Doctoralia website and collecting links to doctor and clinic profiles. It then filters these links to ensure that only gynecologist profiles are considered.

For each profile, the code collects the name, city and phone number. If any of these fields is not found, it returns a question mark. The collected data is stored in a pandas DataFrame.

## Modules Used

- `BeautifulSoup`: Library for parsing and extracting data from HTML and XML.
- `requests`: Library to perform HTTP requests.
- `pandas`: Library for manipulating data in tabular format.
- `re`: Module for handling regular expressions.
- `os`: Module to interact with the operating system, used for deleting auxiliary files.

## Usage

1. **Start Collection**: The code instances the `Collection` class and calls the `start()` method to start collecting data.
2. **Data Collection**: The code navigates through all search results pages and extracts links from gynecologist profiles.
3. **Link Filtering**: It filters links to only include relevant profiles.
4. **Information Collection**: For each profile, it extracts the name, city and phone, storing them in the DataFrame.
5. **Exclusion of Auxiliary Files**: Temporary files created during collection are excluded.
6. **Data Export**: The data is exported to an Excel file named `data.xlsx`.

## Comments

- The code is designed to collect information from the 82 profiles of gynecologists in Belo Horizonte. If the amount of profiles changes, this must be adjusted.
- The code can be adapted for other similar use cases, but remember to check the site's usage policies before web scraping.

## Disclaimer

This code is displayed for educational and informational purposes only. Make sure your use of web scraping complies with the target site's terms of use.
