# Amazon-Reviews-Web-Scrapping
# Amazon Web Scraping and Machine Learning Analysis

## Project Overview
This project involves web scraping product reviews from Amazon for two headphone brands (Beats Solo3 and Sony) and applying machine learning techniques to analyze customer sentiment, compare products, and derive insights into consumer preferences.

## Dataset Description
The scraped data consists of customer reviews for Beats Solo3 and Sony headphones, stored in CSV format:
1. **beats_solo3_amazon_reviews.csv** - Contains customer reviews for Beats Solo3 headphones.
2. **sony_amazon_reviews.csv** - Contains customer reviews for Sony headphones.

### Features in the Dataset:
- **Review Title** – The headline of the customer review.
- **Review Text** – The full review content written by the customer.
- **Star Rating** – The rating given (out of 5 stars).
- **Review Date** – The date when the review was posted.
- **Verified Purchase** – Indicates whether the review was from a verified buyer.
- **Helpful Votes** – Number of people who found the review helpful.

## Web Scraping Process
The data was collected using **BeautifulSoup** and **Scrapy**, following these steps:
1. Sent HTTP requests to Amazon product pages and retrieved HTML content.
2. Parsed relevant elements (title, text, rating, date, etc.).
3. Stored structured data into CSV format.

**Note:** Due to Amazon’s anti-scraping mechanisms, techniques such as user-agent rotation and delays were employed.

## Machine Learning Models and Analysis
The analysis was conducted in `product_comparision.ipynb` and involved the following steps:

### 1. Data Cleaning & Preprocessing
- Removed duplicate and empty reviews.
- Standardized text (lowercasing, removing special characters, stopwords removal, and lemmatization).
- Converted star ratings into sentiment labels (positive, neutral, negative).

### 2. Sentiment Analysis
- **Model Used:** Naïve Bayes Classifier & Logistic Regression.
- **Objective:** Classify reviews as positive, neutral, or negative.
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1-score.

### 3. Product Comparison
- Aggregated sentiment scores to compare Beats Solo3 and Sony headphones.
- Identified common themes in positive and negative reviews using **TF-IDF and WordCloud**.
- Visualized comparative sentiment trends using **Matplotlib and Seaborn**.

### 4. Topic Modeling
- Applied **Latent Dirichlet Allocation (LDA)** to detect common themes in customer reviews.
- Identified topics such as sound quality, battery life, comfort, and price.

### 5. Feature Importance Analysis
- Used **Random Forest** and **SHAP values** to determine key features driving customer sentiment.

## Visualizations & Insights
- **Sentiment distribution across products** - Showcases which product has better customer sentiment.
- **Most frequently mentioned keywords** - Helps understand major pros and cons.
- **WordCloud for each brand** - Provides a visual representation of common words in customer reviews.



