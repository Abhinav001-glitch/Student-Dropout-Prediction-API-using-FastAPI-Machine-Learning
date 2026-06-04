# 🎓 Student Dropout Prediction API

A Machine Learning-powered REST API built using FastAPI that predicts whether a student is likely to drop out based on learning engagement and activity metrics.

## 🚀 Features

* Predicts student dropout risk
* FastAPI-powered REST API
* Interactive Swagger Documentation
* Machine Learning model integration
* JSON-based request and response format
* Easy deployment on Render, Railway, or Docker

## 📊 Input Features

| Feature                | Description                   |
| ---------------------- | ----------------------------- |
| completion_rate        | Course completion percentage  |
| login_frequency        | Average login frequency       |
| last_activity_days_ago | Days since last activity      |
| courses_enrolled       | Number of enrolled courses    |
| forum_posts_count      | Number of forum contributions |

## 🛠 Tech Stack

* Python
* FastAPI
* Scikit-Learn
* NumPy
* Joblib
* Pydantic

## 📂 Project Structure

```text
student-dropout-prediction-api/
│
├── app.py
├── analysis.ipynb
├── student_dropout_model.pkl
├── model_features.pkl
├── student_dataset.xlsx
├── requirements.txt
└── README.md
```

## ▶️ Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/student-dropout-prediction-api.git
cd student-dropout-prediction-api
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the API:

```bash
uvicorn app:app --reload
```

## 🌐 API Endpoints

### Home Endpoint

```http
GET /
```

Response:

```json
{
  "message": "Student dropout prediction is ready."
}
```

### Prediction Endpoint

```http
POST /predict
```

Sample Request:

```json
{
  "completion_rate": 0.45,
  "login_frequency": 3.2,
  "last_activity_days_ago": 12,
  "courses_enrolled": 4,
  "forum_posts_count": 2
}
```

Sample Response:

```json
{
  "prediction": 1
}
```

## 📖 API Documentation

FastAPI automatically generates Swagger documentation:

```text
http://127.0.0.1:8000/docs
```

## 🎯 Use Cases

* Early student intervention
* Educational analytics
* Learning management systems
* Student retention programs
* Academic performance monitoring

## 📜 License

MIT License
