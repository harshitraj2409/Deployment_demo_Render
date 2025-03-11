# Student Placement Prediction - Flask Deployment

## Overview
This project is a **Flask-based web application** for predicting student placement status based on user input parameters such as IQ, CGPA, and academic scores. It utilizes a **pre-trained machine learning model** stored in `model.pkl` to make predictions.

## Directory Structure
```
├── harshitraj2409-deployment_demo_render/
    ├── app.py                # Main Flask application
    ├── model.pkl             # Pre-trained ML model
    ├── requirements.txt      # Dependencies
    └── templates/
        └── index.html        # HTML frontend
```

## Prerequisites
Ensure you have **Python 3.7+** installed on your system. You also need to install the required dependencies before running the application.

## Installation & Setup

1. **Clone the Repository:**
   ```sh
   git clone <repository-url>
   cd harshitraj2409-deployment_demo_render
   ```

2. **Create a Virtual Environment (Recommended):**
   ```sh
   python -m venv venv
   source venv/bin/activate  # On macOS/Linux
   venv\Scripts\activate     # On Windows
   ```

3. **Install Dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

## Running the Application
To start the Flask app, execute:
```sh
python app.py
```
This will launch the application at `http://127.0.0.1:5000/`.

## Application Workflow
1. Navigate to the **home page** (`index.html`).
2. Enter values for **IQ, CGPA, 10th marks, 12th marks, and communication skills**.
3. Click on **Predict** to see the placement prediction.
4. The result will be displayed on the same page.

## API Endpoints
| Route          | Method | Description                                      |
|---------------|--------|--------------------------------------------------|
| `/`           | GET    | Renders the homepage (`index.html`)             |
| `/predict`    | POST   | Accepts form data, makes a prediction, and returns the result |

## Model Details
The `model.pkl` file is a **pickled machine learning model** trained to predict student placements based on the provided input features. Ensure the model is properly serialized using **scikit-learn** before deploying.

## Potential Improvements
- Implement **input validation** to handle missing or incorrect data formats.
- Enhance the UI with **Bootstrap or Material UI** for a better user experience.
- Use a **database (e.g., SQLite, PostgreSQL)** to store past predictions.
- Deploy the app using **Render, Heroku, or AWS** for production use.

## Deployment Guide
To deploy this application on **Render**, follow these steps:
1. Push the project to **GitHub**.
2. Create a new **Render Web Service**.
3. Connect the repository and set the **Start Command**:
   ```sh
   gunicorn app:app
   ```
4. Set **PORT=5000** in environment variables.
5. Click **Deploy** and access the live application.

## License
This project is **open-source** and available under the **MIT License**.

---
Developed by **Harshit Raj**
