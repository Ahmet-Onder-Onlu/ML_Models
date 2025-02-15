# sparkMachineLearning
Project Summary: Data Preprocessing and Modeling
Data Preparation and Cleaning:

Imputing Missing Values: Missing values in the total_bedrooms feature were handled using PySpark’s Imputer function.
Feature Selection and Transformation: Relevant features were selected, and irrelevant or low-impact features were removed. This process is crucial for improving model accuracy.
Feature Encoding:

Encoding Categorical Variables: Categorical variables such as ocean_proximity were converted into numerical values using StringIndexer and OneHotEncoder. This ensures that models can work effectively with categorical data.
Feature Scaling and Vectorization:

Feature Vectorization: Numerical features were combined into a single vector using PySpark’s VectorAssembler function. This allows the model to process all numerical features together efficiently.
Pipeline Structure:

Using Pipeline: PySpark’s Pipeline class was used to automate the sequence of data preprocessing and modeling steps. This allowed for consistency and efficiency across models.
Modeling and Evaluation:

Testing Different Models: Various models such as Linear Regression, Random Forest, GBTRegressor, and Generalized Linear Regression were tested. These models were evaluated using the CrossValidator method for cross-validation.
Hyperparameter Tuning (GridSearch): To optimize the performance of the models, hyperparameters were tuned using ParamGridBuilder and CrossValidator.
Model Performance Evaluation:

RMSE and R² Metrics: Each model's performance was evaluated using the RMSE and R² metrics. These metrics helped assess the accuracy and overall performance of the models.
Visualization of Results:

Performance Comparison: The RMSE and R² values for each model were visualized using bar and line charts. This made it easier to compare the performance of each model.
Saving and Loading the Model:

Selecting and Saving the Best Model: Based on performance results, the best model, GBTRegressor, was saved. This model was stored in a directory using the save() function for future use.
