# Play Tennis Predictor

This project uses a Naive Bayes classifier to predict whether to play tennis based on weather conditions.

## Files

- `PlayTennis.csv`: Dataset with historical weather conditions and decisions to play tennis.
- `assignment4.ipynb`: Python script with functions to calculate probabilities and make predictions.

## Requirements

- Python 3.x
- pandas



## Functions

### `calc_likelihood_probs(data)`
Calculates likelihood probabilities for each feature value given each class.

### `calc_prior_probs(data)`
Calculates prior probabilities of each class.

### `predict(test_sample, likelihood_probs, prior_probs)`
Predicts the class of a test sample using the Naive Bayes classifier.

## Example Output

```sh
--------------------------------------------------
Outlook   Yes   No
Overcast  4/9    0
Rain      1/3  2/5
Sunny     2/9  3/5
--------------------------------------------------
Temperature  Yes   No
Cool         1/3  1/5
Hot          2/9  2/5
Mild         4/9  2/5
--------------------------------------------------
Humidity  Yes   No
High      1/3  4/5
Normal    2/3  1/5
--------------------------------------------------
Wind    Yes   No
Strong  1/3  3/5
Weak    2/3  2/5
--------------------------------------------------

X`= {'Outlook': 'Sunny', 'Temperature': 'Cool', 'Humidity': 'High', 'Wind': 'Strong'}

--------------------------------------------------
P(Outlook=Sunny|Play=Yes) = 2/9
P(Outlook=Sunny|Play=No) = 3/5
--------------------------------------------------
P(Temperature=Cool|Play=Yes) = 1/3
P(Temperature=Cool|Play=No) = 1/5
--------------------------------------------------
P(Humidity=High|Play=Yes) = 1/3
P(Humidity=High|Play=No) = 4/5
--------------------------------------------------
P(Wind=Strong|Play=Yes) = 1/3
P(Wind=Strong|Play=No) = 3/5
--------------------------------------------------
P(Play=Yes) = 9/14
P(Play=No) = 5/14
--------------------------------------------------
P(Yes|X`) = 0.0053
P(No|X`) = 0.0206
--------------------------------------------------
Predicted class of X`: No
```
