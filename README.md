## **📌 README.md for Customer Churn Prediction API**  

Create a file named **`README.md`** in your project folder and add the following content:  

---

# **Customer Churn Prediction API 🚀**  
This is a **Flask-based API** for predicting customer churn. The model is trained using **XGBoost** and deployed on **Render**.  

---

## **📌 Features**
✅ Predicts if a customer will **churn or stay**  
✅ Uses **Machine Learning (XGBoost)** for high accuracy  
✅ REST API for easy integration  
✅ **Deployed on Render** for online access  

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
- Render (for hosting)  

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

url = "http://127.0.0.1:5000/predict"  # Change to your Render URL after deployment
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

## **📌 Deployment on Render**
### **1️⃣ Push Code to GitHub**
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

### **2️⃣ Deploy on Render**
1. Go to [Render](https://render.com)  
2. Click **"New Web Service"** → **"Connect GitHub Repo"**  
3. Select your repository  
4. Set **Build Command:**  
   ```bash
   pip install -r requirements.txt
   ```
5. Set **Start Command:**  
   ```bash
   gunicorn app:app
   ```
6. Click **Deploy** 🚀  

### **3️⃣ Get Your API URL**  
Once deployed, you will get a URL like:  
```
https://churn-prediction.onrender.com
```
Replace `http://127.0.0.1:5000` in the Python request code with this URL.

---

## **📌 Future Improvements**
🔹 Improve model accuracy with **more features**  
🔹 Deploy using **AWS Lambda** for serverless hosting  
🔹 Add a **frontend UI** for user-friendly interaction  

---

## **📌 License**
This project is licensed under the **MIT License**.  

---

### **🎉 Congratulations! Your API is now live! 🚀**  
If you have any questions, feel free to ask! 😊
