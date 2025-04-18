🫀 Heart Disease Risk Prediction Web App
This project presents a user-friendly web application that predicts the risk of heart disease based on clinical parameters. Leveraging machine learning models such as Random Forest, K-Nearest Neighbors (KNN), and Decision Tree, the app provides real-time risk assessments to aid in early detection and prevention.​

📋 Table of Contents
Overview

Features

Dataset

Installation

Usage

Model Evaluation

Technologies Used

Contributing

License

📖 Overview
Cardiovascular diseases remain a leading cause of mortality globally. Early detection is crucial for effective management and treatment. This application allows users to input patient data and receive a prediction regarding the likelihood of heart disease. The backend is powered by machine learning models trained on the UCI Heart Disease dataset.​
GitHub

✨ Features
Interactive User Interface: Built with Streamlit for seamless user experience.

Multiple Model Support: Includes Random Forest, KNN, and Decision Tree classifiers with hyperparameter tuning.

Real-time Predictions: Instant risk assessment upon data submission.

Model Evaluation Metrics: Displays accuracy, F1 score, ROC AUC, and confusion matrix for each model.

Visualization: ROC curves and comparison bar charts for model performance.​
GitHub

📊 Dataset
Source: UCI Machine Learning Repository - Heart Disease Dataset

Attributes:

Age

Sex

Chest Pain Type

Resting Blood Pressure

Cholesterol

Fasting Blood Sugar

Resting ECG

Max Heart Rate Achieved

Exercise Induced Angina

ST Depression (Oldpeak)

Slope of ST Segment

Number of Major Vessels Colored by Fluoroscopy

Thalassemia

Target (Presence of Heart Disease)​
UCI Machine Learning Repository

⚙️ Installation
Clone the Repository:

bash
Copy
Edit
git clone https://github.com/yourusername/heart-disease-prediction.git
cd heart-disease-prediction
Create a Virtual Environment:

bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install Dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run the Application:

bash
Copy
Edit
streamlit run app.py
🚀 Usage
Launch the Streamlit app using the command above.

Input the required patient information in the provided fields.

Click on the Predict button to receive the risk assessment.

View the prediction result along with the confidence score.​

📈 Model Evaluation
The application evaluates and compares the performance of different models using the following metrics:​

Accuracy

F1 Score

ROC AUC Score

Additionally, ROC curves are plotted for visual comparison.​

🛠 Technologies Used
Programming Language: Python

Web Framework: Streamlit

Machine Learning Libraries:

scikit-learn

pandas

numpy

Visualization:

matplotlib

seaborn​

Streamlit


🤝 Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.​
cvd-risk-prediction.streamlit.app


📄 License
This project is licensed under the MIT License.​

