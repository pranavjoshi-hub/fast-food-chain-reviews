# Consumer Review Sentiment Analysis for Fast Food Chains: Project Overview
* Scraped consumer reviews for Subway, McDonald's and Burger King
* Cleaned and feature engineered the data
* Conducted sentiment analysis on the prepared consumer review data
* Stored the data in a remote MongoDB database
* Built a sentiment analysis dashboard

## Code & Resources Used
**Jupyter Notebooks:** Python 3  
**Packages:** pandas, requests, bs4, pymongo, nltk, vaderSentiment  
**Other Tools:** MongoDB Atlas, Power BI Desktop  
**Website Scraped:** https://www.consumeraffairs.com  

## Web Scraping, Feature Engineering & Data Cleaning
First, I scraped 110 consumer reviews for Subway, McDonald's and Burger King each off the website mentioned above.

Then, I feature engineered and cleaned the consumer review data to prepare it for sentiment analysis. The tasks involved are listed below.
* Included only first names of reviewers in 'reviewer' column, while trimming out the rest of the content
* Created new columns
* Removed all punctuation 
* Set all review content to lower-case
* Eliminated all stop-words

## Sentiment Analysis & Data Storage
After the data was prepared, I conducted a sentiment analysis on consumer reviews for each of the 3 fast-food chains. For each of the
reviews, I obtained the polarity scores i.e. the positivity, neutrality and negativity scores of each review for all 3 fast-food chains. Also, a compound score 
was calculated by compounding the 3 polarity scores.  
I also created a new column called 'sentiment' which records the sentiment polarity based on the compound score. Another column 'terms' which
includes a list of all the terms in each review was also created.

The sentiment analysis data was then transferred and stored in a remote MongoDB database called 'Project' within its  collection known as 'SentimentAnalysis'.

## Dashboard
Finally, I created a sentiment dashboard using Power BI. The dashboard displays the following:
* Average polarity (compound score) over time
* Polarity distribution
* Frequent Terms

Here is a screenshot below.  

![](https://github.com/pranavjoshi-hub/fast-food-chain-reviews/blob/main/dashboard_screenshot.PNG)


