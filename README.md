# yelp reviews sentiment analysis

Yelp reviews sentiment analysis is a Python-based project that classifies user reviews by sentiment using machine learning techniques. It leverages Jupyter notebooks to preprocess data, extract features, train models, and evaluate performance. The project compares traditional (Bag of Words + Naive Bayes) and advanced (Word2Vec + LSTM) approaches across two classification tasks: 5-star ratings and 3-class sentiment (positive/neutral/negative).

## features

- **data preprocessing** - cleans raw Yelp review text with tokenization, lemmatization, and stop-word removal
- **feature extraction** - converts text to numerical format using Bag of Words and Word2Vec
- **model training** - trains models with Naive Bayes (BoW) and LSTM (W2V)
- **evaluation** - evaluates model performance using metrics like accuracy, precision, recall, F1 score, and confusion matrix
- **configurable data splits** - supports 70/30 and 80/20 train/test splits
- **Jupyter workflow** - modular structure using 6 notebooks for each step

## getting started

### dependencies

- Python 3.10.0
- Python packages listed in `requirements.txt`

```
pip install -r requirements.txt
```

### installation

- clone the repository or download the zip
- download the Yelp dataset JSON file from [Yelp Open Dataset](https://business.yelp.com/data/resources/open-dataset/)
- place the downloaded file in the `data/` directory
- ensure a virtual environment or Python kernel is set up with the required libraries

### run

- open the `notebooks/` directory
- run the notebooks in the following order:

1. `1_data_preprocessing.ipynb`
2. `2_feature_extraction.ipynb`
3. `3_model_training_BoW_NaiveBayes.ipynb`
4. `3_model_training_Word2Vec_LSTM.ipynb`
5. `4_model_evaluation_BoW_NaiveBayes.ipynb`
6. `4_model_evaluation_Word2Vec_LSTM.ipynb`
   
- in each notebook, use **"Run All"** or step through cells manually

### output

- cleaned data and features saved in `data/`
- trained models saved in `models/`
- evaluation results and confusion matrices displayed within each notebook

## notes

- LSTM + Word2Vec significantly outperforms Naive Bayes + BoW across both classification tasks
- models perform better with 3-class sentiment (positive/neutral/negative) than with 5-star ratings
- changing the train/test split (70/30 vs 80/20) has minimal impact, though 80/20 can slightly improve results
- confusion matrices reveal model biases (e.g., BoW often overpredicts neutral sentiment)

## collaborators

- https://github.com/SirrNick
