# Iris Flower Classification

This repository contains a complete machine learning project for classifying Iris flowers into three species based on sepal and petal measurements. The project includes data preprocessing, exploratory data analysis (EDA), model selection, training, evaluation, and visualization of results. In addition, the repository demonstrates different approaches for target encoding (Label Encoding vs. One-Hot Encoding) and includes an optional PCA-based model for visualization.

## Project Objectives

- **Develop a classification model** to identify Iris flowers into three species using sepal length, sepal width, petal length, and petal width.
- **Identify the most significant features** influencing species classification.
- **Evaluate model performance** using accuracy metrics and confusion matrices.
- **Compare different approaches:**
  - **Label Encoding:** Directly using species labels.
  - **One-Hot Encoding:** Converting species labels into binary vectors.
  - **PCA-Based Modeling:** Reducing features to 2 components for visualization and classification.

## Dataset

The dataset (`IRIS.csv`) includes the following columns:
- `sepal_length`
- `sepal_width`
- `petal_length`
- `petal_width`
- `species` (Iris-setosa, Iris-versicolor, Iris-virginica)

## Repository Structure


## Preprocessing and Exploratory Data Analysis (EDA)

1. **Data Loading:**
   - The dataset is loaded into a pandas DataFrame.
   - Basic dataset information and descriptive statistics are printed.
  
2. **EDA:**
   - Pairplots are generated to visualize the pairwise relationships between features, colored by species.
   - A correlation heatmap shows how features are correlated.
   - A count plot reveals the distribution of species in the dataset.

## Model Selection and Training

### 1. Label Encoding Approach
- **Preprocessing:**
  - Features are standardized using `StandardScaler`.
  - The dataset is split into training (80%) and test (20%) sets.
- **Models Evaluated:**
  - Logistic Regression
  - Random Forest Classifier
  - Support Vector Machine (SVM)
- **Evaluation:**
  - Accuracy and confusion matrices are computed.
- **Results:**
  - Logistic Regression Accuracy: 93.33%
  - Random Forest Accuracy: 90.00%
  - SVM Accuracy: 96.67%

### 2. One-Hot Encoding Approach
- **Preprocessing:**
  - The species target is converted into one-hot encoded vectors.
  - Similar standardization and train-test splitting are applied.
- **Model Evaluated:**
  - Logistic Regression (adapted for multinomial classification)
- **Results:**
  - Logistic Regression (One-Hot Encoding) Accuracy: 93.33%
  
### 3. PCA-Based Modeling (Optional)
- **PCA:**
  - Principal Component Analysis is applied to reduce the four features to 2 components.
  - A scatter plot is created to visualize the data distribution.
- **Modeling:**
  - Logistic Regression is trained using the 2 PCA components.
- **Results:**
  - Accuracy using PCA features is comparable to using all features, while offering visualization benefits.

## Evaluation Results and Discussion

**Model Accuracies Comparison:**
- Logistic Regression: **0.9333**
- Random Forest: **0.9000**
- Support Vector Machine: **0.9667**
- Logistic Regression One-Hot: **0.9333**

**Brief Explanation:**

1. **Label Encoding Approach:**
   - Models trained with label encoded targets learn to map numerical features directly to class labels.
   - In our experiments, Logistic Regression, Random Forest, and SVM all achieved high accuracy.
   
2. **One-Hot Encoding Approach:**
   - Converting species labels into binary vectors (one-hot encoding) allows models (e.g., neural networks) that require this format to be applied.
   - The Logistic Regression model adapted to one-hot targets performed similarly to the label encoded approach. With well-separated classes like Iris, performance differences are minor.

3. **PCA-based Model:**
   - Reducing dimensionality to 2 components offers a clear visualization of the data distribution.
   - Although classification accuracy might slightly differ when using PCA components, it provides insights into the underlying structure and feature importance.

## How to Run the Project

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Aakash-Singh-Git/iris-flower-classification.git
   cd iris-flower-classification
