# 📰 Reddit News Post Analyzer

This project is designed to **scrape**, **analyze**, and **process Reddit posts** from the `r/news` subreddit using NLP techniques. It performs **topic modeling**, **sentiment analysis**, **feature extraction**, and **data preprocessing** for further machine learning tasks.

---

## 🚀 Features

-  Scrapes up to 1000 posts from r/news using PRAW (Reddit API).
-  Performs sentiment analysis using `TextBlob` with Naive Bayes.
-  Extracts primary and secondary topics using **LDA Topic Modeling** from `gensim`.
-  Counts images and hyperlinks in each post.
-  Converts and extracts features from publication time.
-  Applies various scalers (RobustScaler, StandardScaler).
-  Vectorizes textual features using TF-IDF.
-  Saves the dataset to CSV for further analysis or ML.

---

## 📦 Requirements

Make sure to install the required packages:

```bash
pip install praw textblob gensim nltk pandas numpy scikit-learn matplotlib
```
---

## 🔑 Reddit API Setup

Create a Reddit app [here](https://www.reddit.com/prefs/apps) and obtain the following credentials:

- `CLIENT_ID`
- `CLIENT_SECRET`
- `USER_AGENT`

Set them in the script as follows:

```python
import praw

reddit = praw.Reddit(
    client_id='YOUR_CLIENT_ID',
    client_secret='YOUR_CLIENT_SECRET',
    user_agent='YOUR_USER_AGENT'
)
