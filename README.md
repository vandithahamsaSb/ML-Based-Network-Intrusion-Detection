# ML-Based Network Intrusion Detection System

## Overview
This project is a Machine Learning-based Network Intrusion Detection System (NIDS) designed to detect and classify malicious network activities. It helps in identifying attacks or unusual network behavior in real time, providing a robust solution for network security.

The project integrates **ML models**, **FastAPI**, and **MongoDB** to create a full-stack system for monitoring, predicting, and storing network traffic data.

---

## Features
- **Real-Time Detection:** Analyze incoming network data and detect intrusions immediately.
- **Machine Learning Model:** Uses scikit-learn to train and predict network anomalies.
- **Data Storage:** MongoDB stores training and prediction data efficiently.
- **REST API:** FastAPI endpoints allow easy integration and querying.
  - `/train` → Train the model with existing data
  - `/predict` → Upload new network data and get predictions
- **File Upload & Storage:** Supports CSV file uploads for prediction and stores artifacts.
- **Logging & Artifacts:** Keeps detailed logs and saves model artifacts for reproducibility.

---

## Project Structure
Network-Security-ML-System/
├── app.py # FastAPI app entry point
├── main.py # Optional alternative entry point
├── networksecurity/ # Core project modules
│ ├── components/ # Data ingestion, preprocessing, and utilities
│ ├── pipeline/ # Training and pipeline orchestration
│ ├── utils/ # ML and data handling utilities
│ ├── constant/ # Constant values and configuration
│ └── logging/ # Logging setup
├── Artifacts/ # Model and preprocessing artifacts
├── logs/ # Training and prediction logs
├── templates/ # HTML templates for web responses
├── requirements.txt # Python dependencies
└── README.md # Project description

yaml
Copy code

---

## Installation
1. Clone the repository:
```bash
git clone https://github.com/vandithahamsaSb/ML-Based-Network-Intrusion-Detection.git
cd Network-Security-ML-System
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Create a .env file with MongoDB connection string:

ini
Copy code
MONGO_URI=your_mongodb_connection_string
Usage
Run the FastAPI app locally:

bash
Copy code
python app.py
Open your browser and go to http://127.0.0.1:10000/docs to access the interactive API documentation.

Use the endpoints:

Train the model: GET /train

Predict on new data: POST /predict (upload a CSV)

Technologies Used
Python 3.13

FastAPI – API framework

Uvicorn – ASGI server

MongoDB – Database for storing network data

scikit-learn – Machine learning

pandas – Data manipulation

AWS S3 (optional) – For storing prediction files

Docker (optional) – Containerization

Logging and Artifacts
Training logs are saved in the logs/ folder.

Model and preprocessing files are saved in Artifacts/final_model/.

Predicted outputs can be stored in Artifacts/prediction_output/.

Contribution
This repository is maintained solely by Vanditha Hamsa S.B. All commits and contributions are under her account.

