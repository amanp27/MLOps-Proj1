MLOps Project: End-to-End Insurance Vehicle Claim Prediction

🔥 Project Summary

An end-to-end Machine Learning project integrated with MLOps tools and best practices. The project predicts whether a vehicle insurance claim will be made or not, using a structured dataset.

🧱 Project Structure
MLOps-Proj1/
├── src/
│   ├── components/
│   ├── config/
│   ├── pipeline/
│   ├── utils/
│   ├── logger.py
│   └── exception.py
├── config/
│   └── config.yaml
├── artifacts/
├── data/
├── notebooks/
├── Dockerfile
├── .github/workflows/
│   └── main.yml
├── app.py
├── requirements.txt
├── setup.py
└── README.md

🧩 Key Modules

📥 Data Ingestion

Reads raw data (CSV)

Stores it into MongoDB

Dumps it into a local artifact folder for training

✅ Data Validation

Checks schema (column names, nulls, data types)

Creates validation reports

🔄 Data Transformation

Categorical encoding

Feature scaling

Null value treatment

🎓 Model Training

Trains models like Logistic Regression, Random Forest

Saves best model using evaluation metrics (Accuracy, F1-score)

📊 Model Evaluation

Evaluates model performance on test set

Saves reports and metrics (confusion matrix, classification report)

🚀 Model Deployment

Streamlit-based app for UI interaction

Dockerized app

🔁 CI/CD

GitHub Actions for automated testing and deployment

Custom workflows configured in .github/workflows/main.yml

📦 Tech Stack

Language: Python

Model Serving: Streamlit

Data Storage: MongoDB

CI/CD: GitHub Actions

Containerization: Docker

Cloud: AWS S3 (for model artifacts)

⚙️ Installation & Run
# Clone the repo
git clone https://github.com/amanp27/MLOps-Proj1.git
cd MLOps-Proj1

# Create virtual environment & install requirements
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate (Windows)
pip install -r requirements.txt

# Run the application
python app.py

📊 Architecture Diagram
+--------------------+
|     Data Source    |
+---------+----------+
          |
          v
+---------+----------+
|  Data Ingestion    |
+---------+----------+
          |
          v
+---------+----------+
|  Data Validation   |
+---------+----------+
          |
          v
+---------+----------+
| Data Transformation|
+---------+----------+
          |
          v
+---------+----------+
|  Model Training    |
+---------+----------+
          |
          v
+---------+----------+
| Model Evaluation   |
+---------+----------+
          |
          v
+---------+----------+
|   Deployment (UI)  |
+--------------------+


✅ GitHub Actions CI/CD
Sample .github/workflows/main.yml:
name: CI/CD Pipeline

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repo
        uses: actions/checkout@v3

      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.10'

      - name: Install dependencies
        run: |
          pip install -r requirements.txt

      - name: Run tests
        run: |
          pytest


✨ Author

Aman Prajapati
📫 Connect: LinkedIn | GitHub

📜 License

This project is licensed under the MIT License.