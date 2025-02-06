# Sentiment Analysis on IMDB Movie Reviews

##  Sentiment Analysis on IMDB Movie Reviews

### Introduction
In this workshop, sentiment analysis was performed on movie reviews collected from **IMDB**. The dataset consists of reviews for the following movies:
- Chhichhore
- Black Friday
- Kannathil Muthamittal
- Birdemic: Shock and Terror
- Jaane Bhi Do Yaaro

The goal was to analyze the sentiment of these reviews using **VADER** (Valence Aware Dictionary and sEntiment Reasoner) and **Machine Learning (ML)** techniques.

---

## Methodology

### Data Collection
- Reviews were collected from the IMDB website using **web scraping** techniques.
- The `BeautifulSoup` library from `bs4` was used to scrape reviews from the `div` tags with the class `review-container`.
- The scraped data was stored in a Pandas DataFrame with columns: **Ratings** and **Reviews**.

### Data Preparation
- The dataset was preprocessed by:
  - Removing stop words.
  - Converting text to lowercase.
  - Removing special characters and wild characters.
- The preprocessed data was stored in `MameFasseSALL-2441202_3.csv`.

### Sentiment Identification using VADER
- The **Sentiment Intensity Analyzer** from the `VADER` library was used to calculate polarity scores (`neg`, `pos`, `neu`, `compound`).
- Sentiment labels were assigned based on the `compound` score:
  - **Positive**: Compound score ≥ 0.05
  - **Negative**: Compound score ≤ -0.05
  - **Neutral**: Otherwise

### Sentiment Analysis Using Machine Learning
- The dataset was labeled based on the **Ratings** column:
  - **Positive (1)**: Rating > 5
  - **Negative (-1)**: Rating < 5
  - **Neutral (0)**: Rating = 5
- Two vectorization techniques were used:
  - **Bag of Words (BoW)**
  - **TF-IDF**
- Two ML models were trained and tested:
  - **Support Vector Machine (SVM)**
  - **Decision Tree (DT)**

---


## Conclusion
The **Decision Tree (DT)** model with **Bag of Words (BoW)** vectorization achieved the best overall performance for sentiment classification on the movie review dataset. This configuration outperformed other models and settings in terms of precision, recall, F1-Score, and accuracy.

---

## Tools and Libraries Used
- **Python**
- **BeautifulSoup** (for web scraping)
- **Pandas** (for data manipulation)
- **NLTK** (for text preprocessing)
- **VADER** (for sentiment analysis)
- **Scikit-learn** (for ML models and evaluation)

---

## Setup Instructions

### Prerequisites
- Python 3.x
- Required libraries: `pandas`, `numpy`, `bs4`, `nltk`, `vaderSentiment`, `scikit-learn`

### Steps to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/sentiment-analysis.git
   cd sentiment-analysis

2. Install the required libraries:

   ```bash
      pip install -r requirements.txt

### License
This project is licensed under the MIT License. See the LICENSE file for details.