# Mars Project

## Table of Contents
1. [Overview](#overview)
2. [Project Details](#project-details)
   - [Background](#background)
   - [Goals](#goals)
   - [Methodology](#methodology)
   - [Figures](#figures)
3. [Conclusions](#conclusions)
4. [Future Work](#future-work)

## Overview

This project explores the relationship between various weather variables on Mars, such as temperature and pressure, across different Martian months and years. Key questions addressed include: How do temperature and pressure fluctuate over a Martian year? 

## Project Details

### Background

The motivation behind this project is to provide astronauts with insights into the optimal times of the Martian year for space travel. Understanding Martian weather conditions is crucial for planning safe and successful missions. By analyzing fluctuations in temperature and pressure throughout a Martian year, we can determine the best times for landing and conducting operations on Mars. Additionally, the project aims to scrape and analyze Mars news articles to gather valuable information that could aid future research and decision-making.

### Goals

- Scrape titles and preview text from Mars news articles.
- Scrape and analyze Mars weather data from a tabular dataset.

### Methodology

Detailing the approach and methods used to achieve the project's goals:

- **Data Collection:** The URLs scraped for data were:
  - 'https://static.bc-edx.com/data/web/mars_facts/temperature.html' (for Mars weather data)
  - 'https://static.bc-edx.com/data/web/mars_news/index.html' (for Mars news articles)
  - Browser and BeautifulSoup were used to perform the web scraping.

- **Data Cleaning:** The article titles and previews were scraped and stored in a Python dictionary. Mars weather data was scraped from a table, with the scraped data being organized into a list of rows and subsequently stored in a Pandas DataFrame. Upon examining the data types of the columns, it was necessary to convert some columns from objects to appropriate data types such as dates, integers, or floats to facilitate analysis and visualization.

- **Data Storage:** The cleaned data was stored in a CSV file for future use.

- **Data Visualization:** Bar charts were created using Pandas and Matplotlib to visualize the average minimum temperature by month, average pressure by month, and minimum temperature over time.

- **Tools and Libraries:** 
  - **Web Scraping:** Browser and BeautifulSoup.
  - **Data Manipulation:** Pandas.
  - **Data Visualization:** Matplotlib.
  - **Data Verification:** pprint was used to verify the successful scraping of data.

### Figures

#### Figure 0: Mars DataFrame
![Figure 0](https://github.com/pixare7/mars-project/blob/main/images/fig0.png)

*A table displaying the Mars data that was scraped and used for the following visuals.*

#### Figure 1: Average Minimum Temperature by Month
![Figure 1](https://github.com/pixare7/mars-project/blob/main/images/fig1.png)

*A bar chart showing the average minimum temperature per month.*

#### Figure 2: Average Minimum Temperature by Month (Sorted)
![Figure 2](https://github.com/pixare7/mars-project/blob/main/images/fig2.png)

*This sorted bar chart indicates that the third month experiences the lowest average temperatures, while the eighth month has the highest.*

#### Figure 3: Average Pressure by Month
![Figure 3](https://github.com/pixare7/mars-project/blob/main/images/fig3.png)

*A bar chart illustrating the average atmospheric pressure per month.*

#### Figure 4: Average Pressure by Month (Sorted)
![Figure 4](https://github.com/pixare7/mars-project/blob/main/images/fig4.png)

*This sorted bar chart shows that the sixth month has the lowest average pressure, while the ninth month has the highest.*

#### Figure 5: Minimum Temperature Over Time
![Figure 5](https://github.com/pixare7/mars-project/blob/main/images/fig5.png)

*A plot depicting the minimum temperature over time.*

## Conclusions

- The dataset includes 1,867 Martian days of weather data and Mars has 12 months in its year.
- The third month is the coldest, while the eighth month is the hottest.
- On average, the sixth month experiences the lowest atmospheric pressure, while the ninth month has the highest.
- The "Minimum Temperature Over Time" plot reveals a cyclical pattern, with peak temperatures occurring around the estimated days 125, 750, and 1,375. This suggests a seasonal cycle on Mars, with an interval of approximately 625 terrestrial days between these peaks. This implies that a Martian year spans roughly 625 terrestrial days.
- The relationship between temperature and pressure on Mars suggests a cyclical pattern aligned with Martian seasons. Understanding this relationship is crucial for planning missions that minimize risks associated with extreme weather conditions, as selecting the right time for landing and exploration could significantly impact the safety and success of Mars missions.

## Future Work

Future work will involve a deeper exploration of the relationship between temperature and pressure on Mars. Additionally, the data will be further analyzed to determine the best months of the Martian year for travel, based on these weather variables.
