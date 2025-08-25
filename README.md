# Spam Email Detector Using Machine Learning

## Overview
This project demonstrates a spam email detection system using Python and machine learning techniques. It cleans raw email text, extracts relevant features with TF-IDF vectorization, and applies classification algorithms to accurately identify spam.

## Key Components

### Text Cleaning (`clean_text` function)
- Converts all text to lowercase for uniformity.
- Removes punctuation and numbers, replacing them with spaces.
- Removes extra whitespace to prepare clean, consistent input for feature extraction.

### Data Loading and Preparation (`detect_spam` function)
- Loads the dataset CSV file, expects four columns (validation included).
- Drops null values for reliable model training.
- Extracts text and label columns, applies text cleaning, and splits the dataset into training and test sets.

### Feature Extraction (TF-IDF Vectorizer)
- Converts cleaned text into numerical TF-IDF features, limiting to top 1000 features and removing common English stop words.

### Model Training and Evaluation
- Trains multiple models (Naive Bayes and Logistic Regression) on the training data.
- Measures accuracy on the test set and selects the best-performing model.
- Evaluates the best model on the entire dataset.
- Displays a confusion matrix summarizing prediction results.

### New Email Prediction (`predict_new_email` function)
- Preprocesses new input emails.
- Uses the best model to classify new emails as spam or ham.
- Provides prediction confidence scores.

## Usage
Run the main script to train and evaluate models, then use the returned `predict_new_email` function to classify new emails interactively.

## Dependencies
- pandas
- scikit-learn

Install dependencies using:


