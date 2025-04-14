# Rainfall Prediction Web Application

## Overview

This is a Flask-based web application that provides rainfall prediction using multiple machine learning models. The application allows users to input weather parameters and select from various models to get rainfall predictions.

## Features

- User authentication (login/signup)
- Multiple prediction models:
  - Logistic Regression (LR)
  - Random Forest (RF)
  - Artificial Neural Network (ANN)
  - Long Short-Term Memory (LSTM) network
  - CNN-LSTM hybrid model
- API endpoint for programmatic access
- Responsive web interface

## Prerequisites

Before running the application, ensure you have the following installed:

- Python 3.7 or higher
- The following Python packages:
  - flask
  - pandas
  - numpy
  - scikit-learn
  - tensorflow/keras
  - pickle

## Installation

1. Clone the repository or download the source code
2. Install the required packages:
   ```
   pip install flask pandas numpy scikit-learn tensorflow
   ```
3. Ensure all model files are in the same directory as the application:
   - LR_MODEL.pkl
   - RF_MODEL.pkl
   - best_ann_rainfall_model.h5
   - final_lstm_rainfall_model.h5 (optional)
   - final_cnn_lstm_model.h5 (optional)
   - ensemble_model_part_*.h5 (optional, for CNN-LSTM ensemble)

## Running the Application

To start the application, run:
```
python app.py
```

The application will start on `http://localhost:5000` by default.

## Usage

### Web Interface

1. Access the application in your browser at `http://localhost:5000`
2. Login with the default credentials (username: `qwertyuiop`, password: `zxcvbnm`) or create a new account
3. Fill in the weather parameters:
   - Date
   - Location (select from dropdown)
   - Temperature
   - Humidity
   - Wind Speed
   - Precipitation
   - Cloud Cover
   - Pressure
4. Select a prediction model
5. Click "Predict" to get the rainfall prediction

### API Endpoint

You can also make predictions programmatically by sending a POST request to `/predict` with a JSON payload containing the weather parameters. Example:

```bash
curl -X POST -H "Content-Type: application/json" -d '{
    "Date": "2023-05-15",
    "Location": "New York",
    "Temperature": 22.5,
    "Humidity": 65,
    "Wind Speed": 12,
    "Precipitation": 0,
    "Cloud Cover": 40,
    "Pressure": 1012
}' http://localhost:5000/predict?model=lr
```

## Model Information

The application supports the following models:

1. **Logistic Regression (LR)**: Simple linear model for binary classification
2. **Random Forest (RF)**: Ensemble of decision trees
3. **Artificial Neural Network (ANN)**: Multi-layer perceptron
4. **LSTM**: Recurrent neural network for sequence data
5. **CNN-LSTM**: Hybrid convolutional and recurrent neural network

Note: Some models may not be available if their corresponding model files are missing.

## File Structure

- `app.py`: Main application file
- `templates/`: HTML templates for the web interface
  - `home.html`: Main prediction form
  - `login.html`: Login page
  - `signup.html`: Signup page
  - `result.html`: Prediction results page
- Model files (must be in the same directory):
  - LR_MODEL.pkl
  - RF_MODEL.pkl
  - best_ann_rainfall_model.h5
  - final_lstm_rainfall_model.h5
  - final_cnn_lstm_model.h5
  - ensemble_model_part_*.h5

## Configuration

The application can be configured by modifying the following in `app.py`:

- `app.secret_key`: Change this for production use
- `users`: Default user credentials (replace for production)

## Notes

- This is a demo application. For production use:
  - Implement proper user authentication
  - Use a secure secret key
  - Consider using a database for user storage
  - Add proper error handling and logging
- The application creates synthetic historical data for sequence models when actual historical data is not available, which may affect prediction accuracy.

## Troubleshooting

If you encounter errors:
1. Ensure all model files are present
2. Check that all required packages are installed
3. Verify the input data format matches expectations
4. Check the console for error messages when running the application

For LSTM/CNN-LSTM models:
- These require additional preprocessing and may not work if their model files are missing
- The application will still run but will show warnings if these models are not available
