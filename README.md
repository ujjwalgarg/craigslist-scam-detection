# About
Find out whether advertisements of cars and trucks are scam or not.

## Web Scraping

Here are the steps used to scrape data:

###Part 1: URL Extraction of ad listings
- Inspected the HTML structure of Craiglist/Cars+Trucks with Chrome browser’s developer tools
- Deciphered data encoded in URLs
- Used requests and BeautifulSoup for scraping and parsing URL information of each ad listing from the Web
- Stepped through a web scraping pipeline from start to finish
- Built a script that fetches URLs from the website and saved the URLs in Excel
- Saved the URLs scraped from anchor tags of each listing

To create our target URL, split it into two parts:

- The base URL represents the path to the search functionality of the website. The base URL is  https://chicago.craigslist.org/search/chicago-il/cta? This URL directly goes to our desired category of cars and automobiles.
- The specific site location that limits our results for only 60 mile radius of Chicago: “lat=41.7434&lon=-87.7104&search_distance=60”

###Part 2: Data Extraction of ad listings

Traverse through the URLs saved in the previous step and then extracting features like description, price, title, color of the automobile, etc. from each of the links. 

Libraries used:
1.	BeautifulSoup
2.	Requests

## Data Analysis
###Text Pre-Processing:
- Removal of HTML Tags
- Removal of Punctuations 
- Removal of most common words occurring across all the documents 
- Tokenization of sentences
- Lemmatization of tokens (this step was not followed for topic modelling)
- Stopwords removal
- TF-IDF vectorization to finally convert the textual data into numerical vectors

### Topic Modeling
Find the various topics relevant to predicted genuine classified ad on craigslist
