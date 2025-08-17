Project Overview:
A Streamlit-based web application for detecting fraudulent UPI transactions.
Uses a trained XGBoost classification model to predict fraud.
Accepts manual input or CSV file upload for batch prediction.
Allows the user to download predictions as a CSV after processing.

💡 Features:
Predicts whether a UPI transaction is fraudulent or not.
Upload CSV file for batch transaction prediction.
One-click download of processed results with fraud labels.
One-hot encoding for categorical transaction features.
Easy-to-use dropdowns and input fields for manual testing.
Uses a pre-trained model stored as a .pkl file.

🧠 Machine Learning Model:
Model: XGBoost Classifier


Trained on features like:
Transaction amount
Date & time (month/year)
Transaction type, Payment gateway, State, Merchant category
Model is loaded from a pickle file: UPI Fraud Detection Final.pkl

🛠 Tech Stack:
Python
Streamlit (Web UI)
Pandas & NumPy
XGBoost (ML Model)
Altair (optional for visualizations)
Base64 (for CSV downloads)

Install dependencies:
pip install -r requirements.txt

Run the app:
streamlit run app.py


Visit in browser:
Default: http://localhost:8501

📁 File Structure
📦project-folder/
├── app.py                     # Main Streamlit app
├── UPI Fraud Detection Final.pkl  # Trained ML model
├── requirements.txt           # Python dependencies
└── README.md                  # Project description

🧪 Input Data Format (CSV)
If using the CSV upload option, the file should have the following columns:
Date (format: DD-MM-YYYY)
Amount
Transaction_Type
Payment_Gateway
Transaction_State
Merchant_Category

📤 Output:
The app adds a new column: fraud
1 → Fraudulent
0 → Not Fraudulent
Downloadable as a CSV after processing.
