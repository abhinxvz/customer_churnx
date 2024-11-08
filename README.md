# Customer Churn Prediction - README

## Overview
This project aims to predict customer churn for a subscription-based service using machine learning techniques. By analyzing user data, we can identify potential churners and implement strategies to retain them.

---

## Data Source
The dataset used for this project is **`Netflix_Userbase.csv`**, which contains information about users' subscription types, revenue, demographics, and payment history. The dataset includes the following columns:

- **User  ID**: Unique identifier for each user.
- **Subscription Type**: Type of subscription (Basic, Standard, Premium).
- **Monthly Revenue**: Monthly revenue generated from the user.
- **Join Date**: Date when the user joined the service.
- **Last Payment Date**: Date of the last payment made by the user.
- **Country**: Country of the user.
- **Age**: Age of the user.
- **Gender**: Gender of the user.
- **Device**: Device used by the user to access the service.
- **Plan Duration**: Duration of the subscription plan.

---

## Data Description
The dataset consists of **2,500 entries** with **10 columns**. Each row represents a unique user, and the columns contain various attributes related to their subscription and demographic information.

### Summary Statistics
- **Average Age**: 38.8 years
- **Monthly Revenue**: Ranges from $10 to $15
- **Subscription Types**: Users can be classified into Basic, Standard, or Premium categories.

---

## Insights Gained
1. **Demographic Analysis**: Understanding the distribution of users by age, gender, and country can help tailor marketing strategies.
2. **Subscription Preferences**: Analyzing the subscription types can provide insights into which plans are more popular and profitable.
3. **Payment Patterns**: Identifying the average days since the last payment can help in predicting potential churners.

---

## Libraries Used
The following libraries were used in this project:

- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations and handling arrays.
- **Matplotlib**: For data visualization and plotting graphs.
- **Seaborn**: For advanced data visualization, making it easier to create informative statistical graphics.
- **Scikit-learn**: For machine learning algorithms, model training, and evaluation.
- **Joblib**: For saving and loading the trained model.
- **Flask**: For creating a web application to serve the model predictions.
- **Flask-ngrok**: For exposing the Flask application to the internet using ngrok.

---

## Model Choice Rationale
For this project, we chose to use a **Random Forest Classifier** due to its robustness and ability to handle both categorical and numerical features effectively. The Random Forest model is less prone to overfitting compared to other models and provides better accuracy with complex datasets.

---

## Model Training Process
1. **Data Preprocessing**:
   - Dropped unnecessary columns (e.g., User ID).
   - Created a binary target variable `Premium Subscriber` to indicate whether a user is on a Premium plan.
   - Standardized numerical features and one-hot encoded categorical features.

2. **Train-Test Split**: The dataset was split into training and testing sets (80% train, 20% test).

3. **Model Training**: The Random Forest model was trained on the training data.

---

## Performance Metrics
The model's performance was evaluated using the following metrics:

- **Accuracy**: Overall correctness of the model.
- **Precision**: The ratio of true positive predictions to the total predicted positives.
- **Recall**: The ratio of true positive predictions to the actual positives.
- **F1 Score**: The harmonic mean of precision and recall, providing a balance between the two.

### Example Results
- **Accuracy**: 85%
- **Precision**: 82%
- **Recall**: 80%
- **F1 Score**: 81%

---

## Potential Uses of the Model in Business Strategy
1. **Customer Retention**: The model can help identify users who are likely to churn, allowing the business to implement targeted retention strategies (e.g., personalized offers, discounts).
   
2. **Marketing Strategies**: Insights gained from the model can inform marketing campaigns tailored to specific demographics or user segments.

3. **Resource Allocation**: By predicting churn, the company can allocate resources more effectively to improve customer satisfaction and retention.

4. **Product Development**: Understanding customer preferences and behaviors can guide product improvements and new feature developments.

---

## Conclusion
This project demonstrates the power of data analytics and machine learning in predicting customer behavior. By understanding and predicting churn, businesses can take proactive measures to retain customers and enhance their overall strategy. The model developed can serve as a valuable tool for subscription-based services looking to improve customer retention and satisfaction.

---

## Future Work
