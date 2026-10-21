# Decision Tree vs Random Forest - Classification

## Breast Cancer Classification

This project is an end-to-end machine learning classification project that compares the performance of a **Decision Tree Classifier** and a **Random Forest Classifier**.

The objective is to classify breast cancer cases as **Benign** or **Malignant** using different numerical features and compare how a single Decision Tree performs against an ensemble-based Random Forest.

## Dataset

The project uses the **Breast Cancer Wisconsin (Diagnostic) Dataset** from the UCI Machine Learning Repository.

Dataset Source:  
https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic

The dataset contains 569 instances and 30 numerical features computed from digitized images of breast mass samples.

Target classes:

- Benign (B)
- Malignant (M)

## Project Workflow

The project follows the complete machine learning workflow:

1. Dataset loading
2. Data cleaning
3. Missing value and duplicate checking
4. Exploratory Data Analysis (EDA)
5. Target encoding
6. Train-test split
7. Feature selection
8. Decision Tree model training
9. Random Forest model training
10. Model evaluation
11. Performance comparison
12. Data visualization
13. Model saving using Pickle
14. Flask web application for predictions

## Feature Selection

`SelectKBest` with the ANOVA F-test (`f_classif`) is used to select the most relevant features.

To avoid data leakage, the dataset is split into training and testing sets before performing feature selection. The feature selector is fitted only on the training data.

Both models use the same training and testing split to ensure a fair comparison.

## Machine Learning Models

### Decision Tree Classifier

A Decision Tree creates a tree-like structure of decision rules for predicting whether a case belongs to the Benign or Malignant class.

### Random Forest Classifier

Random Forest combines predictions from multiple Decision Trees. This ensemble approach can improve generalization and reduce the overfitting associated with a single tree.

## Evaluation Metrics

The models are compared using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Confusion Matrix
- ROC Curve

These metrics provide a more complete comparison than using accuracy alone.

## Visualizations

The notebook contains visualizations including:

- Target class distribution
- Correlation heatmap
- Selected feature scores
- Confusion matrices
- Decision Tree vs Random Forest performance comparison
- ROC curves
- Random Forest feature importance

## Web Application

A simple Flask web application is included to demonstrate the trained models.

The user enters the required feature values and the application displays predictions from both:

- Decision Tree Classifier
- Random Forest Classifier

The application also displays the predicted malignant probability from each model.

## Project Structure

```text
Decision-Tree-vs-Random-Forest-Classification/
│
├── Classification_Project.ipynb
├── app.py
├── decision_tree_model.pkl
├── random_forest_model.pkl
├── feature_selector.pkl
├── feature_names.pkl
├── selected_features.pkl
├── requirements.txt
│
├── templates/
│   └── index.html
│
└── README.md
```

## Installation

Clone the repository and install the required Python libraries:

```bash
pip install -r requirements.txt
```

## Run the Application

Run the Flask application using:

```bash
python app.py
```

After starting the server, open:

```text
http://127.0.0.1:5000
```

in a web browser.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Flask
- HTML
- CSS
- Pickle
- Google Colab

## Conclusion

This project demonstrates the difference between a single Decision Tree and a Random Forest for a classification problem.

Both algorithms are trained and tested using the same data split and selected features, allowing their performance to be compared fairly using multiple classification metrics.

The Flask application provides a simple practical demonstration of predictions from both trained models.

## Disclaimer

This project is developed for educational and machine learning demonstration purposes only. It is not intended for real-world medical diagnosis or clinical decision-making.
