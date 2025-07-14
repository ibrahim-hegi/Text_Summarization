# Text_Summarization 

## Overview
This project implements a text categorization system for Arabic text data using natural language processing (NLP) techniques and a deep learning model. The system processes Arabic text, applies preprocessing steps, generates word embeddings, and trains a Long Short-Term Memory (LSTM) model to classify text into one of nine categories.

## Dataset
The dataset used is stored in `arabic_categorization_data.csv`, containing Arabic text and corresponding category labels (`type`). The dataset has 10,366 entries with columns:
- `text`: Raw Arabic text.
- `type`: Category label (e.g., culture).

## Project Structure
The project is implemented in a Jupyter Notebook (`TEXT_Summary.ipynb`) and includes the following steps:

### 1. **Import Libraries**
The notebook imports necessary libraries for data processing, NLP, and deep learning, including:
- `pandas` and `numpy` for data manipulation.
- `nltk` for text preprocessing (tokenization, stopword removal, stemming).
- `re` for text cleaning.
- `sklearn` for feature extraction and data splitting.
- `tensorflow.keras` for building and training the LSTM model.
- `gensim` for Word2Vec embeddings.

### 2. **Data Loading**
The dataset is loaded using `pandas` from the CSV file, and the unnecessary `Unnamed: 0` column is dropped.

### 3. **Preprocessing**
The preprocessing pipeline includes:
- **Cleaning**: Removes diacritics, punctuation, numbers, and extra whitespace.
- **Normalization**: Standardizes Arabic characters (e.g., replacing 'أ', 'إ', 'آ' with 'ا').
- **Tokenization**: Splits text into tokens.
- **Stopword Removal**: Removes common Arabic stopwords using `nltk`.
- **Stemming**: Applies
