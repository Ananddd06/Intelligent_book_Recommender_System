# 📚 Intelligent Book Recommender System

## 📌 Project Overview

The **Intelligent Book Recommender System** is designed to analyze book reviews, clean the dataset, extract meaningful insights, perform **sentiment analysis**, and recommend the **top 10 books** based on positive reviews. This project leverages **Natural Language Processing (NLP)** techniques to enhance book recommendations.

---

## 📂 Dataset Description

The dataset consists of book details and user reviews. It includes:

- **Book ID**: Unique identifier for each book.
- **Title**: Name of the book.
- **Author**: Name of the author.
- **Genre**: Category or type of the book.
- **Ratings**: User-provided ratings (1-5 stars).
- **Reviews**: Text-based user feedback about the book.

The dataset requires cleaning and preprocessing to ensure better model performance.

---

## 🧹 Data Cleaning & Preprocessing

Before performing sentiment analysis and recommendations, we process the dataset as follows:

### 1️⃣ Handling Missing Values

- Remove rows with missing **Title**, **Author**, or **Ratings**.
- Fill missing **Genre** values with "Unknown".
- Drop duplicate reviews and books.

### 2️⃣ Text Preprocessing

- Convert text to **lowercase**.
- Remove **punctuation, special characters, and numbers**.
- **Tokenization**: Splitting text into words.
- **Stopword Removal**: Removing common words like "the", "is", etc.
- **Lemmatization**: Converting words to their root form (e.g., "reading" → "read").

### 3️⃣ Handling Ratings

- Convert **ratings** to numerical format.
- Normalize ratings on a scale of **0-1** if needed.

---

## 🏷️ Sentiment Analysis of Books

We analyze the sentiment of book reviews using **Natural Language Processing (NLP)** techniques.

### 🔍 Sentiment Analysis Approach

- **VADER Sentiment Analysis** (for short reviews)
- **TextBlob Polarity Score** (for longer reviews)
- Classify sentiment as:

  - **Positive (Polarity > 0)**
  - **Neutral (Polarity = 0)**
  - **Negative (Polarity < 0)**

- Compute **average sentiment score per book**.
- Higher sentiment scores indicate positive reader feedback.

---

## 📊 Book Recommendation System

We use the following methods to recommend books:

### 📖 1️⃣ Content-Based Filtering

- Uses **TF-IDF (Term Frequency-Inverse Document Frequency)** to recommend books with similar content to a given book.

### ⭐ 2️⃣ Collaborative Filtering

- Analyzes **user preferences and reviews** to recommend books based on similar user interests.

### 📢 3️⃣ Sentiment-Based Recommendations

- Ranks books by **highest positive sentiment scores**.
- Recommends books with:
  - **High positive sentiment**
  - **Good ratings (4+ stars)**
  - **Frequent recommendations by users**

---

## 🔝 Top 10 Book Recommendations

Based on sentiment analysis and ratings, the top 10 recommended books are:

1. **The Alchemist** – Paulo Coelho
2. **Atomic Habits** – James Clear
3. **The Power of Habit** – Charles Duhigg
4. **Harry Potter Series** – J.K. Rowling
5. **The Psychology of Money** – Morgan Housel
6. **Thinking, Fast and Slow** – Daniel Kahneman
7. **To Kill a Mockingbird** – Harper Lee
8. **The Subtle Art of Not Giving a F\*ck** – Mark Manson
9. **Sapiens: A Brief History of Humankind** – Yuval Noah Harari
10. **The 7 Habits of Highly Effective People** – Stephen R. Covey

---

## 💻 Installation & Usage

To run this project locally:

### 📌 Install Dependencies

```bash
pip install pandas numpy nltk scikit-learn textblob vaderSentiment
python recommender.py
```

This `README.md` file provides a detailed guide to dataset cleaning, extraction, sentiment analysis, and recommendations. Let me know if you need modifications! 🚀📖
