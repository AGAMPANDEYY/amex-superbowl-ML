

# T20 Match Prediction Challenge-- Decision Science Track Amex Superbowl-2024

## Overview
This project focuses on developing a machine learning model to predict the winning team in T20 cricket matches using historical data. The model leverages various features derived from player statistics, team performance, and match conditions to enhance prediction accuracy.

![image](https://github.com/user-attachments/assets/ec53797f-53c3-48fa-b202-d7ae2249b40c)


## Introduction
The T20 Match Prediction Challenge is part of the 2024 Amex Campus Super Bowl Competition, where participants are tasked with building a predictive model for T20 cricket matches. This project utilizes sports analytics to provide insights into match outcomes based on historical data.

## Dataset
### Data Sources
The datasets used in this project include:
- **Training Data**: Contains game-level information for training the model (948 rows, 23 columns).
- **Match Level Data**: Scorecards for all games without certain rounds (1689 rows, 30 columns).
- **Batsman Level Data**: Detailed statistics for individual batsmen (24483 rows, 21 columns).
- **Bowler Level Data**: Detailed statistics for individual bowlers (18539 rows, 18 columns).

### Data Description
Each dataset contains unique identifiers for matches, teams, and players along with various performance metrics. The data spans T20 matches from both domestic and international tournaments over recent seasons.

## Features
Key features used in the model include:
- `team_count_50runs_last15`: Ratio of fifties scored by players in the last 15 games.
- `team_winp_last5`: Win percentage ratio of the two teams in their last five games.
- `ground_avg_runs_last15`: Average runs scored at the ground in the last 15 games.

## Modeling
### Algorithms
The following machine learning algorithms are implemented:
- **XGBoost**
- **LightGBM**
- **CatBoost**

These algorithms are selected for their effectiveness in structured data handling and high accuracy in classification tasks.

### Evaluation Metrics
The primary evaluation metric for model performance is accuracy, defined as:

\[
\text{Accuracy} = \frac{\text{Number of correct predictions}}{\text{Total number of predictions}}
\]

## Code Notebook Overview
The code notebook (`ML-Pipeline.ipynb`) encompasses several key components:

- **Data Preprocessing**:
  - Loading and cleaning datasets.
  - Feature engineering to create relevant features such as `team_count_50runs_last15` and `team_winp_last5`.

- **Exploratory Data Analysis (EDA)**:
  - Visualizations to understand feature distributions and relationships with the target variable.
  - Correlation analysis to identify significant predictors.

- **Model Training**:
  - Implementation of XGBoost and LightGBM algorithms.
  - Hyperparameter tuning using cross-validation techniques to optimize model performance.

- **Model Evaluation**:
  - Assessment of model accuracy on training and validation datasets.
  - Comparison of different models to determine the best-performing algorithm based on accuracy metrics.

- **Submission Preparation**:
  - Formatting predictions according to competition requirements.
  - Generating submission files for Round 1 and Round 2 based on model outputs.

## Installation
To set up the project environment, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/t20-match-prediction.git
   cd t20-match-prediction

## Installation

Install the required packages:

```bash
pip install -r requirements.txt
```

## Usage
To run the prediction model:

1. Prepare your dataset according to the specifications outlined in the data description.
2. Execute the main script:

``` bash
python main.py --train_data path/to/train_data.csv --test_data path/to/test_data.csv
The results will be saved in a specified output directory.
```
