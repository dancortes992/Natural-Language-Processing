# Natural-Language-Processing
### Background

This project is part of the Tripleten data science practicum. The focus of this project is natural language processing.

## Project Description

To train a model that automatically detects negative film reviews. Conduct training on three different models as well of composing personally written reviews to test model funcionality. Model must reach an F1 score of 0.85.

**Text Preprocessing tools:** NLTK, SPACY, TF-IDF, BERT

**Models evaluated:** LogisticRegression, LightGBM

**Evaluation metrics:** F1 score, accuracy, precision. ROC-AUC

## Findings

Project shows both logistic regression and LGBM models to be effective for sentiment analysis, with some key takeaways to note:

| Model | Accuracy | F1 | Presicion | ROC AUC |
| --- | --- | --- | --- | --- | 
| NLTK, TF-IDF and LR | 0.88 | 0.88 | 0.95 | 0.95 |
| spaCy, TF-IDF and LR | 0.88 | 0.88 | 0.94 | 0.95 |
| spaCy, TF-IDF and LGBMClassifier | 0.86 | 0.86 | 0.94 | 0.94 |
| BERT and Logistic Regression | 0.88 | 0.88 | 0.95 | 0.95 |
| BERT and LGBMClassifier | 0.86 | 0.86 | 0.94 | 0.93 |

BERT preprocessing with Logistic regression with appears to perform better than other models.
Functionality of models seems to be confirmed when comparing F1 score with review probabilities. As most models appear to predict low probabilities for either one or two reviews that could potentialy be positive. This corelates to the diferent models F1 score of around 0.80.
Probaility prediction versus bipolar sentiment prediction, appears to be better suitied for classifiying movie reviews. This offers greater sentiment distribution not available in bipolar classification. In this case, one could argue model using LGBM from probability prediction is best model. However F1 score still puts logistic regression for bipolar classification higher.

## Software

**Tools:** _python_, _torch_, _tqdm_, _jupyter_

**Libraries:** _pandas_, _NumPy_, _matplotlib_, _scikit-learn_, _seaborn_, _LightGBM_, _NLTK_, _spaCy_, _TF-IDF_
