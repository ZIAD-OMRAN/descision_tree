Decision Tree Classifier for Australian Weather Prediction
This Jupyter Notebook (decision_tree.ipynb) demonstrates the process of building and evaluating a Decision Tree Classifier model to predict whether it will Rain Tomorrow based on various meteorological features from the weatherAUS.csv dataset.

The notebook covers data loading, preprocessing, model training, evaluation, and hyperparameter tuning for the Decision Tree model.

README: Decision Tree Classifier for Australian Weather Prediction
This Jupyter Notebook (decision_tree.ipynb) demonstrates the process of building and evaluating a Decision Tree Classifier model to predict whether it will Rain Tomorrow based on various meteorological features from the weatherAUS.csv dataset.

The notebook covers data loading, preprocessing, model training, evaluation, and hyperparameter tuning for the Decision Tree model.

📚 Table of Contents
Dataset

Dependencies

Data Preparation and Preprocessing

Initial Model Training and Evaluation (Overfitting)

Hyperparameter Tuning for Regularization

Tuning max_depth

Tuning max_leaf_nodes
📊 1. Dataset
The dataset used is weatherAUS.csv, which contains various weather observations for many locations in Australia.

Target Variable: RainTomorrow (Categorical: 'Yes' or 'No').

Features: Includes numerical and categorical features like MinTemp, MaxTemp, Rainfall, Humidity9am, WindGustDir, Location, etc.
💻 2. Dependencies
The following Python libraries are required to run the notebook:

pandas

numpy

matplotlib.pyplot

seaborn

plotly.express (though not used for final plots)

sklearn.model_selection (implicitly used for train/validation/test split via date)

sklearn.impute.SimpleImputer

sklearn.preprocessing.MinMaxScaler

sklearn.preprocessing.OneHotEncoder

sklearn.tree.DecisionTreeClassifier

sklearn.metrics.accuracy_score, confusion_matrix

sklearn.tree.plot_tree, export_text
🛠️ 3. Data Preparation and Preprocessing
The data is processed in the following steps:

Load Data: The weatherAUS.csv file is loaded from Google Drive.

Handle Missing Target Values: Rows with missing values in the target column (RainTomorrow) are dropped.

Time-Series Split: The data is split into Training (before 2015), Validation (2015), and Test (after 2015) sets based on the Date column.

Feature Selection: The date, location, and the target column are separated from the main feature set.

Numerical Feature Handling:

Imputation: Missing numerical values are imputed using the mean strategy (SimpleImputer).

Scaling: Numerical features are scaled to a 0-1 range using MinMaxScaler.

Categorical Feature Handling:

Imputation: Missing categorical values are filled with the placeholder 'unknown'.

One-Hot Encoding: Categorical features (Location, WindGustDir, WindDir9am, WindDir3pm, RainToday) are converted into numerical format using OneHotEncoder.
🌲 4. Initial Model Training and Evaluation (Overfitting)
A Decision Tree Classifier is trained with default settings (max_depth=None, which is unconstrained) on the preprocessed training data.

Training Accuracy: Very high (close to 1.00), which is a sign of overfitting.

Validation Accuracy: Significantly lower, confirming the overfitting issue.



README: Decision Tree Classifier for Australian Weather Prediction
This Jupyter Notebook (decision_tree.ipynb) demonstrates the process of building and evaluating a Decision Tree Classifier model to predict whether it will Rain Tomorrow based on various meteorological features from the weatherAUS.csv dataset.

The notebook covers data loading, preprocessing, model training, evaluation, and hyperparameter tuning for the Decision Tree model.

📚 Table of Contents
Dataset

Dependencies

Data Preparation and Preprocessing

Initial Model Training and Evaluation (Overfitting)

Hyperparameter Tuning for Regularization

Tuning max_depth

Tuning max_leaf_nodes

📊 1. Dataset
The dataset used is weatherAUS.csv, which contains various weather observations for many locations in Australia.

Target Variable: RainTomorrow (Categorical: 'Yes' or 'No').

Features: Includes numerical and categorical features like MinTemp, MaxTemp, Rainfall, Humidity9am, WindGustDir, Location, etc.

💻 2. Dependencies
The following Python libraries are required to run the notebook:

pandas

numpy

matplotlib.pyplot

seaborn

plotly.express (though not used for final plots)

sklearn.model_selection (implicitly used for train/validation/test split via date)

sklearn.impute.SimpleImputer

sklearn.preprocessing.MinMaxScaler

sklearn.preprocessing.OneHotEncoder

sklearn.tree.DecisionTreeClassifier

sklearn.metrics.accuracy_score, confusion_matrix

sklearn.tree.plot_tree, export_text

🛠️ 3. Data Preparation and Preprocessing
The data is processed in the following steps:

Load Data: The weatherAUS.csv file is loaded from Google Drive.

Handle Missing Target Values: Rows with missing values in the target column (RainTomorrow) are dropped.

Time-Series Split: The data is split into Training (before 2015), Validation (2015), and Test (after 2015) sets based on the Date column.

Feature Selection: The date, location, and the target column are separated from the main feature set.

Numerical Feature Handling:

Imputation: Missing numerical values are imputed using the mean strategy (SimpleImputer).

Scaling: Numerical features are scaled to a 0-1 range using MinMaxScaler.

Categorical Feature Handling:

Imputation: Missing categorical values are filled with the placeholder 'unknown'.

One-Hot Encoding: Categorical features (Location, WindGustDir, WindDir9am, WindDir3pm, RainToday) are converted into numerical format using OneHotEncoder.

🌲 4. Initial Model Training and Evaluation (Overfitting)
A Decision Tree Classifier is trained with default settings (max_depth=None, which is unconstrained) on the preprocessed training data.

Training Accuracy: Very high (close to 1.00), which is a sign of overfitting.

Validation Accuracy: Significantly lower, confirming the overfitting issue.


📈 5. Hyperparameter Tuning for Regularization
To mitigate overfitting, hyperparameters that control the complexity of the tree are tuned.

Tuning max_depth
A loop iterates through max_depth values from 1 to 20 to find the setting that minimizes the validation error (i.e., maximizes validation accuracy).

The resulting plot visually compares the training error (which decreases steadily) and the validation error (which initially decreases and then starts to increase due to overfitting).

Resulting Optimal max_depth: The validation error is lowest around max_depth=7 (error ≈0.1546).

Conversation with Gemini
create a readme file to this ipynb notebook

README: Decision Tree Classifier for Australian Weather Prediction
This Jupyter Notebook (decision_tree.ipynb) demonstrates the process of building and evaluating a Decision Tree Classifier model to predict whether it will Rain Tomorrow based on various meteorological features from the weatherAUS.csv dataset.

The notebook covers data loading, preprocessing, model training, evaluation, and hyperparameter tuning for the Decision Tree model.

📚 Table of Contents
Dataset

Dependencies

Data Preparation and Preprocessing

Initial Model Training and Evaluation (Overfitting)

Hyperparameter Tuning for Regularization

Tuning max_depth

Tuning max_leaf_nodes

📊 1. Dataset
The dataset used is weatherAUS.csv, which contains various weather observations for many locations in Australia.

Target Variable: RainTomorrow (Categorical: 'Yes' or 'No').

Features: Includes numerical and categorical features like MinTemp, MaxTemp, Rainfall, Humidity9am, WindGustDir, Location, etc.

💻 2. Dependencies
The following Python libraries are required to run the notebook:

pandas

numpy

matplotlib.pyplot

seaborn

plotly.express (though not used for final plots)

sklearn.model_selection (implicitly used for train/validation/test split via date)

sklearn.impute.SimpleImputer

sklearn.preprocessing.MinMaxScaler

sklearn.preprocessing.OneHotEncoder

sklearn.tree.DecisionTreeClassifier

sklearn.metrics.accuracy_score, confusion_matrix

sklearn.tree.plot_tree, export_text

🛠️ 3. Data Preparation and Preprocessing
The data is processed in the following steps:

Load Data: The weatherAUS.csv file is loaded from Google Drive.

Handle Missing Target Values: Rows with missing values in the target column (RainTomorrow) are dropped.

Time-Series Split: The data is split into Training (before 2015), Validation (2015), and Test (after 2015) sets based on the Date column.

Feature Selection: The date, location, and the target column are separated from the main feature set.

Numerical Feature Handling:

Imputation: Missing numerical values are imputed using the mean strategy (SimpleImputer).

Scaling: Numerical features are scaled to a 0-1 range using MinMaxScaler.

Categorical Feature Handling:

Imputation: Missing categorical values are filled with the placeholder 'unknown'.

One-Hot Encoding: Categorical features (Location, WindGustDir, WindDir9am, WindDir3pm, RainToday) are converted into numerical format using OneHotEncoder.

🌲 4. Initial Model Training and Evaluation (Overfitting)
A Decision Tree Classifier is trained with default settings (max_depth=None, which is unconstrained) on the preprocessed training data.

Training Accuracy: Very high (close to 1.00), which is a sign of overfitting.

Validation Accuracy: Significantly lower, confirming the overfitting issue.

Metric	Score
Training Accuracy (Default Model)	0.9999797
Validation Accuracy (Default Model)	0.7913644
📈 5. Hyperparameter Tuning for Regularization
To mitigate overfitting, hyperparameters that control the complexity of the tree are tuned.

Tuning max_depth
A loop iterates through max_depth values from 1 to 20 to find the setting that minimizes the validation error (i.e., maximizes validation accuracy).

The resulting plot visually compares the training error (which decreases steadily) and the validation error (which initially decreases and then starts to increase due to overfitting).

Resulting Optimal max_depth: The validation error is lowest around max_depth=7 (error ≈0.1546).


Tuning max_leaf_nodes
A loop iterates through powers of 2 for max_leaf_nodes (from 2 to 4096).

Resulting Optimal max_leaf_nodes: The validation error is lowest around max_leaf_nodes=512 (error ≈0.1556).
Conclusion from Tuning: A max_depth of 7 appears to provide the best balance between bias and variance for this model on the validation set.
