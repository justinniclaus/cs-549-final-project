# Spam or Ham Classification

This project that implements an algorithm to classify SMS (or email) messages as **Spam** or **Ham (Legitimate)**. The analysis leverages Natural Language Processing (NLP) techniques to preprocess the data and builds three different machine learning models:
- **Naive Bayes**
- **Support Vector Machines (SVM)**
- **K-Nearest Neighbors (KNN)**

Throughout the notebook, there are detailed steps starting from data loading and exploration, through feature engineering, to model building and evaluation.

## Project Overview

The Jupyter Notebook (`spam_or_ham.ipynb`) walks you through:

1. **Data Loading & Exploration:**
   - The dataset is read from `spam1.csv`, which contains 5,574 SMS messages. The file has two columns:
     - `sms`: Contains the text of the message.
     - `label`: Numerical label where **0** indicates a ham message and **1** indicates a spam message.
   - The notebook provides basic information about the dataset using commands like `df.info()` and displays sample records.

2. **Data Visualization:**
   - A **count plot** using Seaborn is generated to visualize the distribution of spam and ham messages, utilizing a custom color palette.
   - A **pair plot** is created to explore relationships between features.

3. **Feature Engineering:**
   - Three new features are derived from the raw text:
     - **no_of_characters**: Number of characters in a message.
     - **no_of_words**: Number of words (using NLTK’s word tokenizer).
     - **no_of_sentences**: Number of sentences (using NLTK’s sentence tokenizer).
   - These features help provide additional insights that can improve the performance of classification models.

4. **Outlier Analysis:**
   - Visualizations indicate the presence of outliers in the new features. Although not handled within the notebook, this is noted as an important area for further data preprocessing.

5. **Model Building & Comparison:**
   - The notebook sets up the framework to build and compare three distinct machine learning models (Naive Bayes, SVM, and KNN).
   - Each model is evaluated using standard metrics to determine the best approach for classifying messages.

## Requirements

- **Python 3.x**
- Jupyter Notebook or JupyterLab

### Python Libraries

Install the required libraries using pip:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn nltk
