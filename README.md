# Job-Listings-Scraper
## Overview
This project is a web scraping tool designed to collect job listings from LinkedIn. The tool is configured to search for specific job titles, locations, and other parameters, and store the results in a MySQL database. The project leverages Selenium and BeautifulSoup for web scraping, and MySQL Connector for database interactions.

## Features
1. Job Search Configuration Users can specify job titles, locations, and other parameters in a JSON configuration file.

2. Web Scraping: The tool uses Selenium to handle dynamic content loading on LinkedIn's job search pages and BeautifulSoup for parsing the HTML content.

3. Data Storage: Scraped job data, including job titles, company names, job descriptions, locations, links, and posting dates, are stored in a MySQL database.

## How to Use
### Prerequisites
* Python 3.11.5
* Selenium WebDriver (configured for Chrome)
* MySQL database
##### Required Python packages :
* requests
* beautifulsoup4
* mysql-connector-python
* selenium

## Configuration
##### 1. JSON Configuration
The tool is configured using a config.json file.
This file specifies the job titles, locations, and database credentials to be used in the scraping process. Users should update this file with their specific requirements.

##### 2. MySQL Database
* Create a MySQL database named job_listings (or another name as per your configuration).
* The tool will automatically create a jobs table if it doesn't exist, with columns for job ID, title, company, description, location, link, and post date.


## Running the Script
* Ensure that your config.json file is properly configured and placed in the same directory as the script.
* Execute the jupyter notebook after configuring the database and setting up the config.json file.
* The script will launch a Chrome browser instance using Selenium, perform the searches based on the parameters specified, and store the results in the database.

## Limitations
Due to the nature of web scraping, LinkedIn may block or limit requests if too many are made in a short period. This project encountered such a limitation, resulting in an incomplete implementation. The scraping process was interrupted due to a temporary ban, preventing further requests to LinkedIn. This is a common issue with scraping large websites and should be addressed with rate limiting or the use of APIs where available.

## Future Improvements
* Implementing rate limiting to avoid being banned.
* Adding proxy support to distribute requests.
* Expanding support to additional job portals beyond LinkedIn.
  
#### `Disclaimer`
This project is intended for educational purposes only. Scraping data from websites like LinkedIn may violate their terms of service. Please use responsibly and consider the legal implications before proceeding.

  
  
