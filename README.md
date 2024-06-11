# Data_Analysis_Project_1 : Bank Account Closure Prediction Model
1. **Importing Libraries:** First, import the necessary libraries such as pandas for data handling, numpy for numerical operations, matplotlib and seaborn for visualization, and specific modules from scikit-learn for machine learning tasks.

2. **Importing Data:** Load the dataset using the read_csv() function from pandas.

3. **Data Description and Exploration:** To understand the data better, I used methods like **.head()**, **.info()**, and **.describe()** to check its structure, look for missing values, and summarize numerical columns.

4. **Data Preprocessing:** I converted the categorical variables into numerical format. In this code, I replaced categorical variables like 'Geography' and 'Gender' with numerical values. I also handled class imbalance using **_under-sampling_** and _**over-sampling**_ techniques to balance the classes.

5. **Feature Selection:** Define the feature variables (X) and the target variable (y). Here, I select all columns except 'Surname' (because it has no predictive power)and 'Churn'(is my target value) as features (X),to do this I have used **drop()** and 'Churn' as the target variable (y).

6. **Train-Test Split:** Split the data into training and testing sets using **_train_test_split()_** from scikit-learn. This helps in evaluating the model's performance on unseen data.

7. **Data Scaling:** To ensure that all features have the same scale, I standardized the feature variables using _**StandardScaler()**_ from scikit-learn.

8. **Model Building:** I chose the Support Vector Machine (SVM) classifier as the machine learning algorithm. Then, I trained the model on the training data using **_.fit()_**.

9. **Model Evaluation:** After training, I make predictions on the test data using _**.predict()**_. Then, evaluated the model's performance using metrics like confusion matrix, precision, recall, and F1-score.

10. **Hyperparameter Tuning:** I tuned the hyperparameters of the model to improve its performance. Here, I use _**GridSearchCV()**_ from scikit-learn to search for the best combination of hyperparameters.

11. **Observations:** Following data preprocessing, three datasets were generated: the original dataset, one with Random Under Sampling (RUS), and another with Random Over Sampling (ROS). The original dataset was more accurate overall, but it was not as good at identifying customers who had quit. Following hyperparameter tuning greatly improved the model's performance, although at the expense of a slight (4% reduction in total accuracy). The churn recall significantly improved, rising to 41%.

The RUS and ROS models performed similar optimization efforts, producing post-tuning accuracy and recall values that were similar. However, the Hyperparameter tuning for ROS model demonstrated a significant progression, attaining 92% accuracy and a significant 97% churn recall. This significant improvement establishes the Hyperparameter tuning for ROS model as the most successful in achieving the desired result.
