
```markdown
# ANN Customer Churn Prediction

**Repository:** `Ann_classification_churn` by EasySarthak1440

---

## Overview

This project is a **Customer Churn Prediction Web App** built using an **Artificial Neural Network (ANN)** with **TensorFlow/Keras** and deployed using **Streamlit**.

The app takes customer details as input, applies preprocessing (label encoding, one-hot encoding, and feature scaling), and predicts the probability of a customer leaving the bank (churn).

---

## Project Structure

```

Ann_classification_churn/
│── app.py
│── model.h5
│── label_encoder_gender.pkl
│── onehot_encoder_geo.pkl
│── scaler.pkl
│── Churn_Modelling.csv
│── experiments.ipynb
│── prediction.ipynb
│── requirements.txt
│── LICENSE

````

### File Description

- **`app.py`** – Main Streamlit web application  
- **`model.h5`** – Trained ANN model  
- **`label_encoder_gender.pkl`** – Encoder for Gender column  
- **`onehot_encoder_geo.pkl`** – Encoder for Geography column  
- **`scaler.pkl`** – StandardScaler for feature scaling  
- **`Churn_Modelling.csv`** – Original dataset  
- **`experiments.ipynb`** – Model training and experiments notebook  
- **`prediction.ipynb`** – Model testing notebook  
- **`requirements.txt`** – Python dependencies  

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/EasySarthak1440/Ann_classification_churn.git
cd Ann_classification_churn
````

### 2. Create a Virtual Environment (Optional but Recommended)

```bash
python -m venv venv

# For Windows
venv\Scripts\activate

# For macOS/Linux
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Application

Start the Streamlit app using:

```bash
streamlit run app.py
```

Then open the URL shown in the terminal (usually):

```
http://localhost:8501
```

---

## Features

The app accepts the following user inputs:

* Geography (One-Hot Encoded)
* Gender (Label Encoded)
* Age
* Credit Score
* Balance
* Estimated Salary
* Tenure
* Number of Products
* Has Credit Card (0/1)
* Is Active Member (0/1)

It returns:

* **Churn Probability**
* **Final Prediction** (Likely to churn / Not likely to churn)

---

## How the Model Works

1. User inputs are collected via Streamlit UI.
2. Categorical values are encoded using saved encoders.
3. Geographic features are one-hot encoded.
4. Numerical features are scaled using `StandardScaler`.
5. The processed data is passed to the ANN model (`model.h5`).
6. The model outputs the churn probability.

---

## Retraining the Model

If you want to retrain and save a new model:

```python
model.save('model.h5')

import pickle
with open('label_encoder_gender.pkl', 'wb') as f:
    pickle.dump(label_encoder_gender, f)

with open('onehot_encoder_geo.pkl', 'wb') as f:
    pickle.dump(onehot_encoder_geo, f)

with open('scaler.pkl', 'wb') as f:
    pickle.dump(scaler, f)
```

---

## License

This project is licensed under the MIT License.

---

## Author

**Sarthak Kelkar**
GitHub: [https://github.com/EasySarthak1440](https://github.com/EasySarthak1440)

```
