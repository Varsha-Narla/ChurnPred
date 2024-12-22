# ChurnPred
This is a Flask based web API for predicting customer churn using machine learning. The model predicts whether a customer will churn based on various factors. The model is trained using a random forest classifier and is saved as a .pkl file. 

Features:
1. Customer Churn Prediction : Predicts if a customer is likely to churn based on input features
2. API Endpoint : a POST request endpoint /predict_churn where users can send customer data in JSON format for prediction

## Project Structure

- **app.py**: Main Flask application that serves the API for churn prediction.
- **random_forest_model.pkl**: Trained machine learning model for churn prediction (needs to be loaded by the API).
- **gender_map.pkl**: Encodes gender categories (e.g., Male, Female).
- **payment_method_map.pkl**: Encodes payment methods (e.g., Credit, Debit).
- **scaler.pkl**: Scales numerical features for the model.
- **requirements.txt**: A list of Python dependencies required to run the project.
- **.gitignore**: Specifies files and directories to be ignored by Git (e.g., model files).
- **README.md**: This file, providing details on setting up and using the API

 ## Setup Instructions
Before running the application, you need to have **Python 3.6+** installed. You also need to install the necessary dependencies
Clone the repository to your local machine.
Download the model files - random_forest_model.pkl, gender_map.pkl, payment_method_map.pkl, scaler.pkl. 
Run the Flask Application 
Test the API using Postman: 
Set the URL to http://127.0.0.1:5000/predict_churn
In the Body tab, select raw and then JSON. Provide input data in the following format :
    {
  "Gender": "Female",
  "Age": 35,
  "Tenure": 12,
  "MonthlyCharges": 70.50,
  "TotalCharges": 800.00,
  "PaymentMethod": "Credit",
  "ServiceUsage1": 10,
  "ServiceUsage2": 15,
  "ServiceUsage3": 20
    }

Click send to get the churn value. 

Send a JSON object with the following fields : 
Gender: Customer's gender (e.g., "Male", "Female")
Age: Customer's age (integer)
Tenure: Number of months the customer has been with the service (integer)
MonthlyCharges: Customer's monthly charges (float)
TotalCharges: Customer's total charges (float)
PaymentMethod: Payment method used by the customer (e.g., "Credit", "Debit")
ServiceUsage1, ServiceUsage2, ServiceUsage3: Service usage metrics (float)

For more information/questions, please reach out to n.varsha.official@gmail.com
