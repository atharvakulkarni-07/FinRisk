# Investment Risk Prediction

This project aims to predict investment risk using historical financial data. The goal is to classify days as either "risky" or "not risky" based on various financial indicators. This project utilizes machine learning techniques to achieve high accuracy in risk prediction.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Feature Engineering](#feature-engineering)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Results](#results)
- [Usage](#usage)
- [Requirements](#requirements)
- [Installation](#installation)
- [Contributing](#contributing)


## Project Overview

This project leverages machine learning to predict investment risks. By analyzing historical financial data, it aims to forecast whether a particular day will be risky or not. A logistic regression model is used to classify the risk based on various financial metrics, achieving an accuracy of approximately 97%.

## Dataset

The dataset used in this project includes the following columns:
- `Date`: The date of the record
- `Open`: Opening price of the stock
- `High`: Highest price of the stock during the day
- `Low`: Lowest price of the stock during the day
- `Close`: Closing price of the stock
- `Volume`: The trading volume
- `Name`: Name of the stock

After preprocessing, the dataset is expanded with additional features:
- `Return`: Daily return
- `MA20`: 20-day moving average of the closing price
- `MA50`: 50-day moving average of the closing price
- `Volatility`: 20-day rolling standard deviation of the daily returns

The target variable `Risk` is defined as:
- `1` (Risky) if the daily return is less than -1.5%
- `0` (Not Risky) otherwise

## Feature Engineering

Several new features are created to enhance the predictive power of the model:
- **Daily Return**: Calculated as the percentage change in the closing price from the previous day.
- **Moving Averages**: 20-day and 50-day moving averages of the closing prices to capture trends.
- **Volatility**: 20-day rolling standard deviation of daily returns to capture the market's volatility.

## Model Training and Evaluation

The dataset is split into training (70%) and testing (30%) sets. A logistic regression model is trained using the training data. The model's performance is evaluated using the testing data with the following metrics:
- **Accuracy**: 92%

## Results

The logistic regression model achieved an accuracy of 97%, demonstrating its effectiveness in predicting investment risks based on historical financial data.

## Usage

To use this project, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/investment-risk-prediction.git
    cd investment-risk-prediction
    ```

2. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

3. Run the Jupyter notebook to train the model and make predictions:
    ```sh
    jupyter notebook investment_risk_prediction.ipynb
    ```

## Requirements

- Python 3.6+
- Jupyter Notebook
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn

## Installation

1. Ensure you have Python 3.6+ installed.
2. Clone the repository and navigate into the project directory.
3. Install the required packages using pip:
    ```sh
    pip install -r requirements.txt
    ```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
