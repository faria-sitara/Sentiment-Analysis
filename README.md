# 📘 Sentiment Analysis on Amazon Reviews

This project applies **Natural Language Processing (NLP)** and multiple sentiment analysis techniques to analyze and compare customer reviews from Amazon.  
The goal is to classify text into **positive**, **neutral**, or **negative** sentiment, visualize trends, and compare different sentiment models such as **VADER**, **TextBlob**, and **RoBERTa**.

---

## 📊 Project Overview

The project focuses on:

- Preprocessing and cleaning review data  
- Exploratory Data Analysis (EDA) with visualizations  
- Sentiment analysis using:
  - VADER (Valence Aware Dictionary for Sentiment Reasoning)
  - TextBlob
  - RoBERTa (transformer-based model)
- Comparing model outputs across star ratings  
- Visualizing insights with Matplotlib and Seaborn  
- Highlighting review texts with unexpected sentiment patterns  

---

## 🛠️ Key Features and Workflow

### 🔹 1. Data Cleaning & Preprocessing
- Removed missing values and filtered ratings to 1–5 stars  
- Tokenized and lemmatized text using **NLTK**  
- Performed POS tagging and named entity recognition  

### 🔹 2. Exploratory Data Analysis (EDA)
- Bar charts showing review counts by star rating  
- **Word Cloud** to display most frequent words  

### 🔹 3. Sentiment Analysis Models

#### ✅ VADER
- Lexicon-based model from **NLTK**  
- Provides **compound**, **pos**, **neu**, and **neg** scores  

#### ✅ TextBlob
- Calculates **polarity** and **subjectivity** scores  
- Simple API for rule-based sentiment detection  

#### ✅ RoBERTa  
Model: `cardiffnlp/twitter-roberta-base-sentiment`  
- Pre-trained transformer model via **HuggingFace**  
- Tokenized text and predicted probabilities for:
  - `roberta_neg`
  - `roberta_neu`
  - `roberta_pos`  

### 🔹 4. Comparative Analysis
- Merged sentiment scores with metadata  
- Visualized:
  - Sentiment distributions by review score  
  - Boxplots comparing model outputs by star rating  
  - Pair plots showing correlations among sentiment dimensions  

### 🔹 5. Review Highlighting
- Retrieved reviews where models gave **surprisingly high or low sentiment scores** within 1-star or 5-star reviews  

---

## 📦 Tech Stack

- Python  
- Pandas, NumPy  
- NLTK, TextBlob  
- Matplotlib, Seaborn  
- WordCloud  
- HuggingFace Transformers  
- Scikit-learn  
- Jupyter Notebook  
