
# **Customer Churn Prediction API 🚀**  
This is a **Flask-based API** for predicting customer churn. The model is trained using **XGBoost** and can be used locally.  

---

## **📌 Features**
✅ Predicts if a customer will **churn or stay**  
✅ Uses **Machine Learning (XGBoost)** for high accuracy  
✅ REST API for easy integration  

---

## **📌 Technologies Used**
- Python  
- Flask  
- Scikit-learn  
- XGBoost  
- Joblib  
- Pandas  
- NumPy  
- Gunicorn (for production deployment)  

---

## **📌 Installation & Setup**
### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/YOUR_USERNAME/churn-prediction-api.git
cd churn-prediction-api
```

### **2️⃣ Install Dependencies**
```bash
pip install -r requirements.txt
```

### **3️⃣ Run the Flask App Locally**
```bash
python app.py
```
The API will start at **http://127.0.0.1:5000** 🚀  

---

## **📌 API Endpoints**
| Endpoint | Method | Description |
|----------|--------|------------|
| `/` | GET | Returns API status |
| `/predict` | POST | Predicts churn for a customer |

---

## **📌 How to Use the API**
### **Send a POST request to `/predict` with JSON input**  

#### **Example Request:**
```json
{
    "tenure": 12,
    "MonthlyCharges": 70,
    "TotalCharges": 840,
    "Contract_Two year": 1,
    "InternetService_Fiber optic": 1,
    "PaymentMethod_Electronic check": 1
}
```

#### **Example Python Code to Send Request**
```python
import requests

url = "http://127.0.0.1:5000/predict"
data = {
    "tenure": 12,
    "MonthlyCharges": 70,
    "TotalCharges": 840,
    "Contract_Two year": 1,
    "InternetService_Fiber optic": 1,
    "PaymentMethod_Electronic check": 1
}

response = requests.post(url, json=data)
print(response.json())
```

#### **Expected Response:**
```json
{
    "churn_probability": 0.76,
    "churn_prediction": 1
}
```
(1 → Customer will churn, 0 → Customer will stay)

---

## **📌 Future Improvements**
🔹 Improve model accuracy with **more features**  
🔹 Deploy using **Render or AWS** for online access  
🔹 Add a **frontend UI** for user-friendly interaction  

---

