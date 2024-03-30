## Tweets Sentiment Analysis

This repository contains code for performing sentiment analysis on tweets using machine learning techniques. The dataset used for this analysis can be found on [Kaggle](https://www.kaggle.com/paakhim10/tweets-and-engagement-metrics).

### Usage

1. **Installing Dependencies**: 
   Before running the code, make sure to install the required Python packages. You can install them using the following commands:
   ```
   %pip install nltk
   %pip install pandas
   %pip install scikit-learn
   %pip install -U imbalanced-learn
   %pip install gensim
   %pip install kaggle
   %pip install matplotlib
   %pip install seaborn
   ```

2. **Downloading the Dataset**:
   To download the dataset from Kaggle, you can use the Kaggle API. First, make sure you have the API credentials set up. Then run the provided script to download and extract the dataset:
   ```python
   import os
   import zipfile

   os.system('kaggle datasets download -d paakhim10/tweets-and-engagement-metrics')
   with zipfile.ZipFile('tweets-and-engagement-metrics.zip', 'r') as zip_ref:
       zip_ref.extractall('')
   ```

3. **Reading and Preprocessing the Dataset**:
   The dataset is then read into a Pandas DataFrame and preprocessed to clean the text data. This includes converting text to lowercase, removing URLs, usernames, punctuation, and numbers, as well as tokenization and stemming.

4. **Labeling Dataset Using VADER**:
   The NLTK library's VADER (Valence Aware Dictionary and sEntiment Reasoner) module is used to label the dataset with sentiment scores.

5. **Analyzing the Dataset**:
   The dataset is analyzed to understand the distribution of sentiment categories and to check if it's balanced.

6. **Feature Extraction**:
   Two methods of feature extraction are employed: TF-IDF (Term Frequency-Inverse Document Frequency) and Word2Vec. TF-IDF vectorization converts text data into numerical features, while Word2Vec represents words in vector space.

7. **Naive Bayes Model**:
   A Naive Bayes classifier is trained using the combined features extracted from TF-IDF and Word2Vec. The model is evaluated using various metrics, including precision, recall, and F1-score.

### Files Included

- `tweets-engagement-metrics.csv`: The dataset containing tweets and engagement metrics.
- `sentiment_analysis.ipynb`: Jupyter Notebook containing the complete code for sentiment analysis.
- `check.csv`: CSV file containing the processed text and sentiment scores for analysis.

Feel free to explore the provided code and dataset to understand how sentiment analysis is performed on Twitter data. If you have any questions or suggestions, please don't hesitate to reach out.
