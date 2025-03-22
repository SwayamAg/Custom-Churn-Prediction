# Custom-Churn-Prediction-Tuned-Version  
### Churn Prediction Using Deep Learning - Tuned Version  

## 📌 Project Overview  
This is the **tuned version** of my customer churn prediction project, where I improved the model’s accuracy from **80% to 86%** through **hyperparameter tuning, regularization, and architectural adjustments**.  

### 🎯 Key Highlights:  
- Enhanced **Sequential Neural Network** using **TensorFlow & Keras**  
- Applied **L2 Regularization & Dropout**  
- Increased the number of layers and fine-tuned hyperparameters  
- Improved **accuracy from 80% to 86%**  
- Trained for **100 epochs** with optimized batch size  

---

## 📂 Dataset Information  
The dataset remains the same, containing customer details such as **Geography, Credit Score, Age, Balance, etc.**  

### 🔑 Features Used:  
| Feature Name        | Description                            |  
|---------------------|----------------------------------------|  
| **CreditScore**      | Customer's credit score                |  
| **Geography**        | Country of residence                   |  
| **Gender**           | Male/Female                            |  
| **Age**              | Customer's age                         |  
| **Tenure**           | Years of account ownership             |  
| **Balance**          | Account balance                        |  
| **NumOfProducts**    | Number of bank products used           |  
| **HasCrCard**        | Whether the customer has a credit card |  
| **IsActiveMember**   | Whether the customer is active         |  
| **EstimatedSalary**  | Estimated salary                       |  

### 🎯 Target Variable:  
- **`Exited`** (1 = Churn, 0 = No Churn)  

---

## 🔨 Model Architecture (Tuned Version)  
```python
# Tuned neural network  
model = Sequential([  
    Input(shape=(X_train.shape[1],)),  
    Dense(64, activation='relu', kernel_regularizer=tf.keras.regularizers.l2(0.01)),  
    Dropout(0.3),  
    Dense(32, activation='relu', kernel_regularizer=tf.keras.regularizers.l2(0.01)),  
    Dropout(0.3),  
    Dense(1, activation='sigmoid')  
])

---

# Churn Prediction (Tuned Version)  
Improved model performance by tuning hyperparameters, reducing overfitting, and enhancing learning stability.  

---

## 🛠 **Tuned Hyperparameters**  
- **Optimizer**: Adam  
- **Loss Function**: Binary Crossentropy  
- **Epochs**: 100  
- **Batch Size**: 64  
- **L2 Regularization**: 0.01  
- **Dropout**: 30%  

---

## 📊 **Results & Observations**  
- **Accuracy on Test Set**: **~86%**  
- 🔵 Reduced **overfitting** with **regularization & dropout**  
- 🔵 Enhanced the **model’s learning** by increasing layers and adjusting batch size  
- 🔵 Achieved **more stable accuracy and loss curves**  

---

## 🧠 **Learning Takeaways**  
- 🎯 **Hyperparameter tuning** and **regularization** improved overall model performance  
- 🛡️ Adding **Dropout layers** reduced overfitting significantly  
- 🔧 Increasing **network complexity** carefully boosted learning for non-linear data  

---

## 📁 **Repository Structure**   

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

