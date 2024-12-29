# Big Data Analysis: Scarping and Sentiment Analysis on Play Store Reviews

## Project Overview

This project focuses on performing sentiment analysis on Google Play Store reviews for popular social media applications. We scraped, cleaned, and analyzed a total of 160,000 reviews across four apps: Instagram, X (formerly Twitter), Reddit, and Snapchat. The primary objective was to extract insights about user sentiments and to perform exploratory data analysis (EDA) on the reviews.

## Key Objectives

- **Data Scraping**: Gather user reviews from the Google Play Store for each app using `google-play-scraper`.
- **Data Cleaning**: Preprocess and clean the raw review data for meaningful analysis.
- **Sentiment Analysis**: Classify reviews into positive, negative, and neutral sentiments.
- **Exploratory Data Analysis (EDA)**: Discover trends, patterns, and insights from the cleaned dataset.

## Tools and Technologies

- **Programming Language**: Python
- **Libraries**:
  - Data Scraping: `google-play-scraper`
  - Data Manipulation: `pandas`, `numpy`
  - Data Visualization: `matplotlib`, `seaborn`
  - Sentiment Analysis: `TextBlob`, `NLTK`
  - Cleaning and Preprocessing: `re` (regular expressions), `scikit-learn`

## Dataset Details

- **Source**: Google Play Store
- **Applications**: Instagram, X, Reddit, Snapchat
- **Total Reviews Scraped**: 160,000 (40,000 reviews per app)

### Raw Data Fields

1. `reviewId`: Unique identifier for each review
2. `userName`: Name of the reviewer
3. `userImage`: URL to the reviewer's profile image
4. `content`: Review text
5. `score`: Rating given by the user (1-5 stars)
6. `thumbsUpCount`: Number of likes on the review
7. `reviewCreatedVersion`: App version during the review
8. `at`: Timestamp of the review
9. `replyContent`: Developer's reply to the review (if any)
10. `repliedAt`: Timestamp of the developer's reply
11. `appVersion`: App version at the time of the review

### Cleaned Data Fields

1. `reviewId`: Unique identifier for each review
2. `userName`: Name of the reviewer
3. `content`: Cleaned review text
4. `score`: Rating given by the user (1-5 stars)
5. `thumbsUpCount`: Number of likes on the review
6. `reviewCreatedVersion`: App version during the review
7. `at`: Timestamp of the review
8. `sentiment`: Sentiment classification (Positive, Negative, Neutral)

## Data Cleaning Process

- Removed duplicate and irrelevant entries.
- Handled missing values.

## Sentiment Analysis

- **Approach**: Sentiment scores were derived using the Hugging Face Transformers library with pre-trained models like BERT for sentiment classification.
- **Sentiment Classes**:
  - Positive: Reviews with a polarity score > 0
  - Neutral: Reviews with a polarity score = 0
  - Negative: Reviews with a polarity score < 0

## Exploratory Data Analysis (EDA)

- Analyzed the distribution of ratings and sentiments for each app.
- Discovered insights into user preferences and common complaints.
- Compared sentiment trends across apps.
- Visualized metrics like `thumbsUpCount` and review timestamps.

### Visualizations Included

- Distribution of review scores for each app.
- Sentiment distribution pie charts.
- Time-series trends of review sentiment.
- Bar charts comparing the average `thumbsUpCount` for different sentiments.

## Project Workflow

1. Data scraping using `google-play-scraper`.
2. Data cleaning and preprocessing using `pandas` and `re`.
3. Sentiment analysis using `TextBlob` for polarity-based classification.
4. EDA to extract and visualize insights using `matplotlib` and `seaborn`.

## Repository Structure

```
├── data
│   ├── raw_data
│   ├── cleaned_data
├── notebooks
│   ├── BDA.ipynb
│   ├── Graphs and Visualizations.ipynb
├── README.md
```

## How to Run the Project

1. Clone the repository.
2. Run the scripts or notebooks in the `notebooks` folder.


