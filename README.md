# Amazon-Web-Scraper

- This project details an Amazon web scraping solution developed in Python. It demonstrates extracting product title and price information
from an Amazon product page and storing it in a CSV file, with a mechanism to track price changes over time.

## Features

- Web Scraping: Utilizes BeautifulSoup and requests to parse HTML content and extract relevant product data.
- Data Extraction: Specifically targets product title and price from Amazon product pages.
- Persistent Storage: Stores the scraped data (Title, Price, Date) in a CSV file named AmazonWebScraperDataset.csv.
- Automated Price Tracking: Includes a function check_price() that can be set to run daily, appending new price and date entries to the CSV, allowing for historical price analysis.
- HTML Parsing from Local File: Addresses Amazon's scraping restrictions by demonstrating a workaround to parse an HTML page downloaded locally.

## Technologies Used

- Python
- BeautifulSoup (for HTML parsing)
- Requests (for making HTTP requests - though direct scraping was restricted by Amazon)
- Pandas (for data analysis and displaying the CSV content)
- CSV module (for reading and writing CSV files)
- Datetime (for managing timestamps)

## Setup and Usage

- Clone the repository (if hosted on GitHub).
- Install dependencies:
- Bash
- pip install beautifulsoup4 requests pandas
- Download the Amazon product HTML: Due to Amazon's scraping restrictions, you will need to manually save the HTML of the desired Amazon product page (e.g., https://www.amazon.com/Funny-Data-Systems-Business-Analyst/dp/B07FNW9FGJ) as amazon_product.html in the same directory as the script.
- Run the script: The check_price() function can be called to perform the scraping and data appending.
- Python

## Example of running the price check once
-     check_price()
- To run daily (uncomment and run in a persistent environment)
-     while(True):
-          check_price() 
-          time.sleep(86400) # checks price everyday to see if it changes
The script will create or append to AmazonWebScraperDataset.csv.
