# Sentiment Analysis with spaCy and scikit-learn

This repository implements a sentiment analysis model on reviews from Yelp, Amazon, and IMDb.
senti.webp
## Overview:

The system starts by preprocessing the data using **spaCy**, an advanced NLP library. Features include:
- Tokenization
- Sentence splitting
- Stop word removal
- Lemmatization
- Parts of Speech (POS) tagging
- Named Entity Recognition (NER)

Following this, the cleaned data is vectorized using the `TfidfVectorizer` and fed into a `LinearSVC` model from **scikit-learn** to predict sentiments.

## Code Walkthrough:

1. **Data Importing and NLP Preprocessing**
    - Load spaCy's English model
    - Tokenize the data
    - Sentence splitting using custom pipeline component
    - Display named entities and dependencies using `displacy`

2. **Data Loading and Initial Exploration**
    - Load the Yelp, Amazon, and IMDb datasets
    - Append these datasets together
    - Check for missing values
    - Basic exploratory data analysis

3. **Text Data Cleaning Function**
    - Remove stopwords
    - Perform lemmatization
    - Discard punctuation marks

4. **Model Training and Evaluation**
    - Split the data into training and test sets
    - Vectorize the reviews using `TfidfVectorizer`
    - Use a `LinearSVC` classifier
    - Train the classifier
    - Predict sentiments on the test set
    - Evaluate using classification report and confusion matrix

5. **Model Testing**
    - Predict sentiments for custom reviews

## Requirements:

- spaCy
- scikit-learn
- pandas

## Installation:

1. Clone the repository.
2. Install the necessary libraries:
   ```bash
   pip install spacy scikit-learn pandas
   ```

3. Run the provided code using Jupyter Notebook or any Python environment.
4. Modify or test with custom reviews as needed.

## Contributing:

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. Please ensure to update tests as appropriate.

## License:

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements:

Thanks to the creators of spaCy, scikit-learn, and the providers of the Yelp, Amazon, and IMDb datasets.

## Future Work:

- Hyperparameter tuning for better accuracy
- Incorporating other classifiers or deep learning models
- Expanding the dataset for improved model generalization

