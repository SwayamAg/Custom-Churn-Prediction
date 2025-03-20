# Custom-Churn-Prediction# Churn Prediction Using Deep Learning - First Attempt

## 📌 Project Overview
This is my first attempt at predicting customer churn using a **Deep Learning model** built with **TensorFlow & Keras**. The dataset used is **Churn_Modelling.csv**, and the goal is to classify whether a customer will exit (churn) or stay with the bank.

### 🎯 Key Highlights:
- Built a **Sequential Neural Network** with **TensorFlow/Keras**
- Achieved **~80% accuracy**
- Applied **One-Hot Encoding & Feature Scaling**
- Used **ReLU & Sigmoid activations**
- Trained for **100 epochs**

---

## 📂 Dataset Information
The dataset consists of customer details, such as **Geography, Gender, Credit Score, Balance, etc.**

### 🔑 Features Used:
| Feature Name | Description |
|-------------|-------------|
| **CreditScore** | Customer's credit score |
| **Geography** | Country of residence |
| **Gender** | Male/Female |
| **Age** | Customer's age |
| **Tenure** | Years of account ownership |
| **Balance** | Account balance |
| **NumOfProducts** | Number of bank products used |
| **HasCrCard** | Whether the customer has a credit card |
| **IsActiveMember** | Whether the customer is active |
| **EstimatedSalary** | Estimated salary |

### 🎯 Target Variable:
- `Exited` (1 = Churn, 0 = No Churn)

---

## 🔨 Model Architecture
```python
# Build the neural network
model = Sequential([
    Input(shape=(X_train.shape[1],)),
    Dense(3, activation='relu'),
    Dense(11, activation='relu'),
    Dense(1, activation='sigmoid')
])
```

### **Hyperparameters**
- **Optimizer**: Adam
- **Loss Function**: Binary Crossentropy
- **Epochs**: 100
- **Validation Split**: 20%

---

## 📊 Results & Observations
- **Accuracy on Test Set:** ~80%
- **Validation Accuracy fluctuated** across epochs
- The model could be **further optimized** by adjusting layers, neurons, and hyperparameters.

### 📉 Accuracy & Loss Curves:
![loss_vs_val_loss](https://github.com/user-attachments/assets/844e0ef6-2d4f-4acd-89c3-c3b483610683)
![accuracy_vs_val_acc](https://github.com/user-attachments/assets/a233749e-007c-4189-941f-30e4827d50b7)



---

## 📌 Next Steps
✅ **Hyperparameter Tuning** (Neurons, Layers, Regularization, Dropout)
✅ **Reduce Overfitting** (Better architecture)
✅ **Increase Accuracy** (Aim for 85-90%)

---

## 📜 Learning Takeaways
📌 Neural networks **require careful tuning** to improve performance.
📌 **Feature scaling & encoding** are crucial for better training.
📌 **Churn prediction** can benefit from additional feature engineering.

---

## 📎 Repository Structure
```
📂 Churn_Prediction_DL
├── 📄 Churn_Modelling.csv
├── 📄 churn_prediction.ipynb
├── 📄 requirements.txt
├── 📄 README.md  
```

---

## 📦 Installation & Requirements
To install dependencies, run:
```bash
pip install -r requirements.txt
```

### **requirements.txt**
```
tensorflow
keras
numpy
pandas
matplotlib
scikit-learn
```

---

## 📌 Future Update (86% Accuracy Version) 🚀
I plan to **improve this model** with better hyperparameter tuning & architecture adjustments. Stay tuned for a follow-up post! 🎯

📌 **[Follow me on LinkedIn]([your-linkedin-profile-link](https://www.linkedin.com/in/swayam-agarwal/)) for updates!** 😊

