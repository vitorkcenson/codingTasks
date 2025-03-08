# Titanic Survival Prediction with Decision Trees

## Description

This project demonstrates the use of Decision Tree classifiers to predict passenger survival on the Titanic, based on the well-known Titanic dataset. The code performs data preprocessing, feature engineering, model training, and evaluation. It explores the impact of `max_depth` on model performance and visualizes the decision tree. Learning how to build and tune decision tree models is crucial for understanding classification tasks and is a fundamental concept in machine learning. This task illustrates how to handle missing values, encode categorical features, and evaluate model performance using training, development, and test datasets.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Data Preprocessing](#data-preprocessing)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Visualization](#visualization)
- [Results](#results)
- [Credits](#credits)

## Installation

1.  **Python:** Ensure you have Python 3.x installed. You can download it from [python.org](https://www.python.org/downloads/).
2.  **Dependencies:** Install the required libraries using pip:

    ```bash
    pip install pandas numpy scikit-learn matplotlib ipython
    ```

## Usage

1.  **Download the Dataset:** Download the `titanic.csv` dataset and place it in the same directory as the Python script.
2.  **Run the Script:** Execute the Python script:

    ```bash
    python titanic_decision_tree.py
    ```

3.  **View Results:** The script will output the accuracy of the model on the development and test sets, as well as generate a line graph comparing training and development accuracies for different `max_depth` values. It will also produce a visualized decision tree as a plot.

## Data Preprocessing

The script performs the following data preprocessing steps:

-   Loads the Titanic dataset from `titanic.csv`.
-   Removes unnecessary columns (`Cabin`, `Name`, `SibSp`, `Parch`, `Ticket`).
-   Applies one-hot encoding to the `Sex` and `Embarked` columns to convert categorical features into numerical ones.
-   Splits the data into training, development, and test sets.

## Model Training and Evaluation

-   The code trains a Decision Tree Classifier using the training data.
-   It evaluates the model's performance on the development set to tune the `max_depth` hyperparameter.
-   It iterates through different `max_depth` values (2 to 10) and records the training and development accuracies.
-   Finally, it trains a Decision Tree with `max_depth=4` and evaluates it on the test set to report the final accuracy.

## Visualization

-   The script generates a visualization of the trained Decision Tree, showing the decision rules and feature importance.
-   It also produces a line graph comparing the training and development accuracies for different `max_depth` values, allowing for easy identification of overfitting or underfitting.

## Results

The script outputs the following results:

-   Development set accuracy for the initial training.
-   Training and development accuracies for `max_depth` values from 2 to 10.
-   A line graph illustrating the training and development accuracies.
-   Test set accuracy for the final model with `max_depth=4`.

Example output:

Development Set Accuracy: 0.8189655172413793
Training Decision Tree with max_depth = 2
Training Decision Tree with max_depth = 3
Training Decision Tree with max_depth = 4
Training Decision Tree with max_depth = 5
Training Decision Tree with max_depth = 6
Training Decision Tree with max_depth = 7
Training Decision Tree with max_depth = 8
Training Decision Tree with max_depth = 9
Training Decision Tree with max_depth = 10

Results:
max_depth: 2, Train Accuracy: 0.8039, Dev Accuracy: 0.7978
max_depth: 3, Train Accuracy: 0.8258, Dev Accuracy: 0.8157
max_depth: 4, Train Accuracy: 0.8357, Dev Accuracy: 0.8157
max_depth: 5, Train Accuracy: 0.8520, Dev Accuracy: 0.8090
max_depth: 6, Train Accuracy: 0.8652, Dev Accuracy: 0.8090
max_depth: 7, Train Accuracy: 0.8751, Dev Accuracy: 0.8090
max_depth: 8, Train Accuracy: 0.8914, Dev Accuracy: 0.7978
max_depth: 9, Train Accuracy: 0.9013, Dev Accuracy: 0.7921
max_depth: 10, Train Accuracy: 0.9112, Dev Accuracy: 0.8034
Test Set Accuracy (max_depth = 4): 0.7937

![Line Graph of Accuracy vs Max Depth](your_graph_screenshot.png)
![Decision Tree Visualization](your_tree_screenshot.png)

(Remember to replace `your_graph_screenshot.png` and `your_tree_screenshot.png` with actual paths to your saved screenshots.)

## Credits

This project was created by:

-   Vitor Kratz Censon - https://github.com/vitorkcenson/
