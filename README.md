# Customer Churn Prediction Using ANN

This project predicts customer churn using an Artificial Neural Network (ANN). Churn prediction helps businesses identify customers who are likely to leave, enabling proactive retention strategies.

---

## 📁 Dataset

The dataset used is `Churn_Modelling.csv` which contains the following variables:

- `RowNumber`
- `CustomerId`
- `Surname`
- `CreditScore`
- `Geography`
- `Gender`
- `Age`
- `Tenure`
- `Balance`
- `NumOfProducts`
- `HasCrCard`
- `IsActiveMember`
- `EstimatedSalary`
- `Exited` (target variable: 1 = customer left, 0 = customer stayed)

---

## 🛠 Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- TensorFlow / Keras
- Streamlit
- Matplotlib
- TensorBoard

---

## ⚙️ Features

- **Numerical Features:** CreditScore, Age, Tenure, Balance, NumOfProducts, EstimatedSalary  
- **Categorical Features:** Gender, Geography, HasCrCard, IsActiveMember  
- **Target:** Exited (binary classification)

---

## 🔧 Preprocessing Steps

1. Dropped unnecessary columns: `RowNumber`, `CustomerId`, `Surname`.  
2. Encoded categorical variables:
   - `Gender` → Label Encoding  
   - `Geography` → One-Hot Encoding  
3. Scaled features using `StandardScaler`.  
4. Saved encoders and scaler as `.pkl` files for deployment.

---

## 🧠 Model Architecture

A simple feedforward ANN using Keras:

- **Input Layer:** Number of neurons = number of features  
- **Hidden Layer 1:** 64 neurons, ReLU activation  
- **Hidden Layer 2:** 32 neurons, ReLU activation  
- **Output Layer:** 1 neuron, Sigmoid activation  

**Loss Function:** Binary Crossentropy  
**Optimizer:** Adam  
**Metrics:** Accuracy  

**Callbacks:**  
- EarlyStopping (monitors `val_loss`)  
- TensorBoard for training visualization  

---

## 🚀 Training

- Training/Test split: 80% / 20%  
- Epochs: 100  
- Early stopping used to avoid overfitting  
- TensorBoard logs saved in `logs/fit/`  

---

## 💾 Saving the Model

The trained model is saved as:

- `model.h5` → ANN model  
- `scaler.pkl` → StandardScaler  
- `label_encoder_gender.pkl` → LabelEncoder for Gender  
- `onehot_encoder_geo.pkl` → OneHotEncoder for Geography  

---

## 🎥 Project Demo
🎬 **Watch the demo video below:**  


https://github.com/user-attachments/assets/f0429740-c33a-48e0-ae93-4f8b277a8dcc

