# Wine-Classification-Models-using-R

## Overview
This project focuses on classifying wines into two categories based on their color: red or white. The analysis is conducted using various classification techniques in R, utilizing libraries for data manipulation, modeling, and visualization. The dataset used for this analysis is the Wine Quality Dataset from the UCI Machine Learning Repository.

## Data Description
'winequality-red.csv' and 'winequality-white.csv' contain the dataset. It comprises various attributes of wines, including chemical properties and quality ratings. For this analysis, the datasets for red and white wines are used separately. Each dataset includes several variables, such as volatile acidity and total sulfur dioxide, which are used as features for the classification models.

## File Structure

- `winequality-red.csv`: The csv file containing the dataset.
- `winequality-white.csv`: The csv file containing the dataset.
- `wine_classify.Rmd`: The R Markdown file containing all the code, descriptions, and visualizations.

## Libraries Used
- `tibble`: For creating and manipulating tibbles, a modern version of data frames in R.
- `tidyverse`: A collection of R packages designed for data science.
- `dplyr`: For data manipulation using a consistent set of verbs.
- `ggplot2`: For creating static graphics.
- `MASS`: For linear and quadratic discriminant function analysis.
- `FNN`: For fast k-nearest neighbor search algorithms and applications.

## Implementation Details

### Data Loading and Preprocessing
- Red and white wine datasets are loaded from the UCI Machine Learning Repository.
- The datasets are converted to tibbles and a new column indicating the color of the wine is added to each dataset.
- The datasets are split into training and testing sets, ensuring a balanced representation of both wine colors.

### Exploratory Data Visualization
- A scatter plot is created to visualize the relationship between volatile acidity and total sulfur dioxide for both red and white wines in the training set.
- A binary variable representing the wine color is created for model training and evaluation.

### Model Training
- Four classification models are trained using the training data:
  - Logistic Regression: A linear model for binary classification.
  - Linear Discriminant Analysis (LDA): A method for finding a linear combination of features that best separate the classes.
  - Quadratic Discriminant Analysis (QDA): Similar to LDA but allows for non-linear separation of classes.
  - K-Nearest Neighbors (KNN): A non-parametric method used for classification, with models trained for k=3 and k=9.

### Model Prediction and Visualization
- The trained models are used to make predictions on the testing set.
- Scatter plots are created to visualize the actual and predicted wine colors from each model.

### Error Calculation
- Classification error rates are calculated for both the training and testing sets for each model.
- The results are summarized in a table, highlighting the performance of each model.

## How to Run
1. Ensure that R and all the required libraries are installed.
2. Open the R Markdown file in RStudio or any other R Markdown editor.
3. Run the chunks in the R Markdown file sequentially to perform the analysis and generate the visualizations.

## Conclusion
This project demonstrates the application of various classification techniques to a wine quality dataset, with the goal of classifying wines based on their color. The models' performances are evaluated using classification error rates, and the results are visualized to provide insights into the dataset and the modeling techniques used. LDA, Logistic Regression, and QDA are found to perform better compared to the KNN models in this particular scenario.
