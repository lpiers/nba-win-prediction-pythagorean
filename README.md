# NBA Win Prediction with Pythagorean Expectation

Predicts NBA game outcomes using the Pythagorean win expectation formula
(borrowed from sabermetrics) and logistic regression, evaluated against
actual 2017-18 season results.

## What this does
- Builds a Pythagorean win% metric per team from cumulative points for/against
- Fits a logistic regression (GLM, binomial) predicting game-level win/loss
- Extends the model with home-court advantage as a second predictor
- Evaluates both models with confusion matrices and classification accuracy
- Tests out-of-sample: does 1st-half-season win% (raw or Pythagorean) predict
  2nd-half performance?

## Results
- Pythagorean win% alone predicts wins with ~65% accuracy
- Adding home-court advantage improves classification accuracy further
- Pythagorean win% from the first half of the season is a stronger
  predictor of second-half performance than raw win% 

## Tech
Python, pandas, statsmodels (GLM/OLS), scikit-learn (LogisticRegression,
confusion_matrix, classification_report), seaborn

## Data
NBA game-level box scores, 2017-18 season
