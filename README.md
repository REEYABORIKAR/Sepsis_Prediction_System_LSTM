Sepsis Prediction System
This project is a Flask-based web application that utilizes a Long Short-Term Memory (LSTM) deep learning model to predict the risk of sepsis in patients based on physiological data.

Project Structure
The project is organized as follows:

app.py: The main Flask application script that handles file uploads, model inference, and rendering the web interface.

scripts/:

data_preprocessing.py: Contains functions to load, clean, and normalize .psv clinical data files for training.

train_model.py: Script to build, train, and save the LSTM model.

templates/:

index.html: The frontend interface for uploading patient data and viewing results.

utils.py: Helper functions for real-time data preprocessing, generating patient summaries, and interpreting risk levels.

.gitignore: Specifies files and directories to be ignored by Git, such as virtual environments and Python caches.

Features
File Upload: Accepts patient data in .psv (pipe-separated values) format.

Real-time Prediction: Uses a trained LSTM model to calculate a sepsis risk percentage.

Risk Categorization: Classifies risk into three levels:

Low: Risk score < 30%.

Moderate: Risk score between 30% and 70%.

High: Risk score ≥ 70%.

Visualizations: Generates a graph showing the sepsis risk trend over time.

Patient Summary: Displays key statistics such as Average Heart Rate, Maximum White Blood Cell count, and Minimum Mean Arterial Pressure.

Clinical Interpretation: Provides recommendations based on the predicted risk level.

Installation and Setup
Environment: It is recommended to use a virtual environment.

Dependencies: Ensure flask, pandas, numpy, tensorflow, matplotlib, and scikit-learn are installed.

Model Training:

Place training data in a data/ folder.

Run python scripts/train_model.py to train and save the model to models/lstm_model.h5.

Running the App:

Execute python app.py.

Access the application at http://127.0.0.1:5000/.

Usage
Navigate to the web interface.

Upload a .psv file containing patient physiological data.

Click "Predict" to view the risk analysis, trend graph, and clinical summary.