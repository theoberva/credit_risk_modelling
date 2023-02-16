# Probability of Default Model

![](https://www.commercialriskonline.com/wp-content/uploads/2022/05/Credit-risk_shutterstock_1832810149.jpg)

This project is an implementation of a probability of default model, which is used to predict the likelihood that a borrower will default on a loan. The model is trained on a dataset of historical loan data and can be used to make predictions on new loan applications. The Logistic model was created using fine and coarse classing utilizing weight of evidence and information values.

The model was evaluated using the ROC curve, Gini coefficient, and Kolmogorov-Smirnov test. The final output is an easy-to-use scorecard that ranges from 300 to 850.

## Table of Contents

- [Data](#data)
- [Preprocessing](#preprocessing)
- [Feature Engineering](#feature-engineering)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)
- [Scorecard](#scorecard)
- [Contributing](#contributing)
- [License](#license)

## Data

The dataset used for this project is sourced from [LendingClub](https://www.lendingclub.com/) and consists of historical data on loans issued by the platform. The data includes information such as loan amount, interest rate, borrower income, and credit score, as well as whether the loan was fully paid off or defaulted.

The dataset can be found in the `data` directory and is split into separate training and testing sets.

## Preprocessing

Before training the model, the data is preprocessed to ensure that it is in the correct format and that any missing values are handled appropriately. The preprocessing steps include:

- Dropping irrelevant columns
- Handling missing values
- Converting categorical features into numerical features using one-hot encoding
- Scaling numerical features

The preprocessing code can be found in the `preprocessing.py` file.

## Feature Engineering

In addition to preprocessing, we also perform feature engineering to create new features that may be more informative than the original features. The feature engineering steps include:

- Creating new features based on the original features (e.g., debt-to-income ratio)
- Removing redundant features
- Using domain knowledge to create new features (e.g., calculating the number of delinquent accounts)

The feature engineering code can be found in the `PD_Model.ipynb` file.

## Model Training

The model is trained using a logistic regression algorithm, which is a popular algorithm for binary classification problems such as this one. The training code can be found in the `PD_Model.ipynb` file.

## Model Evaluation

The trained model is evaluated on the testing set to assess its performance. The evaluation metrics used include the ROC curve, Gini coefficient, and Kolmogorov-Smirnov test. The evaluation code and results can be found in the `PD_Model.ipynb` file.

## Scorecard

The final output is an easy-to-use scorecard that ranges from 300 to 850. Fine and coarse classing with weight of evidence and information values were used to create the binning for the variables on the scorecard.

## Contributing

If you would like to contribute to this project, feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License.
