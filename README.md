# Sentiment Classification on Financial Tweets

Predicting the sentiment expressed in finance-related tweets — negative, positive or
neutral — and comparing how a range of classifiers handle the task.

The work runs in two passes. The first treats it as a binary problem, negative sentiment
against everything else, and uses it to compare algorithms, select features and tune
hyperparameters. The second returns to the full three-class problem, evaluated by
cross-validation.

## Data

TODO — state the source, the number of tweets and the class distribution.

Labels: `0` negative, `1` positive, `2` neutral. The class balance is worth stating
explicitly: if neutral dominates, a weighted f1-score can look respectable while the
model barely recognises the minority class, and that shapes how every figure below
should be read.

## Models compared

Logistic regression, k-nearest neighbours, random forest, a neural network, and two
approaches not covered in the course (TODO — name them). All are trained on the same
explanatory variables so the comparison holds, and each is reported with precision,
recall, weighted f1-score, fit time and its main hyperparameters.

Text representation: TODO — describe how the tweets become features (tokenisation,
TF-IDF, embeddings, whatever was used). This is the choice that moves the results most,
and it deserves a sentence or two.

| Model | Precision | Recall | Weighted f1 | Time |
|---|---|---|---|---|
| Logistic regression | | | | |
| k-NN | | | | |
| Random forest | | | | |
| Neural network | | | | |
| TODO | | | | |
| TODO | | | | |

## Optimisation

**Features.** Test error tracked as the set of explanatory variables changes, for one
model.

**Hyperparameters.** Test error tracked across the hyperparameter grid, for two models.

## Selected model

TODO — which model, and why: algorithm, hyperparameters, features. Reported with its
precision, recall, weighted f1-score and correct classification rate, a ROC curve, and a
calibration curve showing whether its predicted probabilities can be taken at face value.

Known weaknesses: TODO. This section is worth writing honestly — a model that fails
predictably on sarcasm, on tickers it has never seen, or on the minority class is more
useful to a reader than one described as working well.

## Multi-class

The three-class problem, with cross-validation. TODO — method and results.

## Repository

```
financial-tweet-sentiment/
├── notebooks/
│   └── analysis.ipynb
├── data/
├── figures/            # ROC, calibration, error curves
└── report.pdf
```

Built in Google Colab. TODO — list the libraries (scikit-learn, pandas, …).

## Context

Machine Learning project — Aix-Marseille University, Master in Economics (M1),
2025–2026. Group project.
