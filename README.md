# ❤️ Heart Disease Prediction using Machine Learning

## 📌 Project Overview

This project is a Machine Learning classification system that predicts the presence of heart disease based on patient health-related features.

The project uses **Logistic Regression** to classify patients into two categories:

- **0 → No Heart Disease**
- **1 → Heart Disease**

The project follows a complete Machine Learning workflow, including data preprocessing, data analysis, feature and target separation, train-test splitting, model training, model evaluation, and prediction on new patient data.

---

## 🎯 Objectives

- Analyze the heart disease dataset.
- Perform data preprocessing and basic data analysis.
- Separate input features and the target variable.
- Split the dataset into training and testing sets.
- Train a Logistic Regression classification model.
- Evaluate the model using accuracy score.
- Predict heart disease for new patient data.

---

## 🔄 Project Workflow

```text
Heart Disease Dataset
        ↓
Data Preprocessing
        ↓
Data Analysis
        ↓
Feature & Target Separation
        ↓
Train-Test Split
        ↓
Logistic Regression
        ↓
Model Training
        ↓
Model Evaluation
        ↓
New Patient Data
        ↓
Prediction
```

---

## 📊 Dataset

The dataset contains **303 records and 14 columns**, consisting of **13 input features and 1 target variable**.

### Features

| Feature | Description |
|---|---|
| `age` | Age of the patient |
| `sex` | Sex of the patient |
| `cp` | Chest pain type |
| `trestbps` | Resting blood pressure |
| `chol` | Serum cholesterol |
| `fbs` | Fasting blood sugar |
| `restecg` | Resting electrocardiographic results |
| `thalach` | Maximum heart rate achieved |
| `exang` | Exercise-induced angina |
| `oldpeak` | ST depression induced by exercise |
| `slope` | Slope of the peak exercise ST segment |
| `ca` | Number of major vessels |
| `thal` | Thalassemia-related feature |

### Target Variable

| Value | Meaning |
|---|---|
| `0` | No Heart Disease |
| `1` | Heart Disease |

---

## 🛠️ Technologies Used

- **Python**
- **NumPy**
- **Pandas**
- **Scikit-learn**
- **Logistic Regression**
- **Google Colab / Jupyter Notebook**

---

## ⚙️ Machine Learning Implementation

### 1. Data Preprocessing

The heart disease dataset is loaded and analyzed using Pandas.

The dataset is inspected to understand its:

- Dimensions
- Data types
- Statistical information
- Missing values
- Target variable distribution

### 2. Feature and Target Separation

The `target` column is separated from the input features.

```python
X = heart_data.drop(columns='target', axis=1)
Y = heart_data['target']
```

Where:

- `X` represents the input features.
- `Y` represents the target variable.

### 3. Train-Test Split

The dataset is divided into training and testing datasets using an **80:20 ratio**.

The project uses:

- **80% Training Data**
- **20% Testing Data**
- `stratify=Y`
- `random_state=2`

```python
X_train, X_test, Y_train, Y_test = train_test_split(
    X,
    Y,
    test_size=0.2,
    stratify=Y,
    random_state=2
)
```

### 4. Logistic Regression Model

A Logistic Regression model is created and trained using the training dataset.

```python
model = LogisticRegression()

model.fit(X_train, Y_train)
```

### 5. Model Evaluation

The model performance is evaluated using **Accuracy Score**.

```python
X_train_prediction = model.predict(X_train)

training_data_accuracy = accuracy_score(
    X_train_prediction,
    Y_train
)
```

The same approach is used to evaluate the model on the testing dataset.

---

## 📈 Model Performance

The Logistic Regression model achieved the following accuracy:

| Dataset | Accuracy |
|---|---:|
| Training Data | **85.12%** |
| Testing Data | **81.97%** |

The model achieved **81.97% accuracy on the test dataset**.

---

## 🔮 Prediction on New Data

After training the model, it can be used to predict the presence of heart disease for new patient data.

### Example Input

```python
input_data = (
    44, 1, 0, 120, 169, 0, 1,
    144, 1, 2.8, 0, 0, 1
)
```

The input data is converted into a NumPy array and reshaped before making the prediction.

```python
input_data_as_numpy_array = np.asarray(input_data)

input_data_reshaped = input_data_as_numpy_array.reshape(1, -1)

prediction = model.predict(input_data_reshaped)
```

### Prediction Classes

- **0 → No Heart Disease**
- **1 → Heart Disease**

---

## 📁 Project Structure

```text
Heart-Disease-Prediction-using-Machine-Learning/
│
├── heart_disease_data.csv
├── Heart_Disease_Prediction.ipynb
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/YandapalliTejaswini/-Heart-Disease-Prediction-using-Machine-Learning.git
```

### 2. Navigate to the Project Directory

```bash
cd -Heart-Disease-Prediction-using-Machine-Learning
```

### 3. Install Required Libraries

```bash
pip install numpy pandas scikit-learn
```

### 4. Open the Notebook

Open `Heart_Disease_Prediction.ipynb` using **Google Colab** or **Jupyter Notebook**.

### 5. Run the Notebook

Run the notebook cells sequentially to perform:

1. Data loading
2. Data preprocessing
3. Data analysis
4. Feature and target separation
5. Train-test splitting
6. Model training
7. Model evaluation
8. Prediction on new data

---

## 📚 Key Concepts

This project demonstrates the practical implementation of:

- Python Programming
- NumPy
- Pandas
- Data Preprocessing
- Data Analysis
- Feature and Target Separation
- Train-Test Split
- Stratified Sampling
- Logistic Regression
- Binary Classification
- Model Training
- Accuracy Evaluation
- Prediction on New Data

---

## 🚀 Future Enhancements

- Compare multiple classification algorithms.
- Apply feature scaling.
- Perform hyperparameter tuning.
- Implement cross-validation.
- Add a confusion matrix.
- Evaluate precision, recall, and F1-score.
- Build an interactive Streamlit application.
- Deploy the application online.

---

## ⚠️ Disclaimer

This project is developed for **educational and learning purposes only**.

The predictions generated by this model should not be considered a medical diagnosis or a substitute for professional medical advice.

Medical decisions should always be made by qualified healthcare professionals.

---

## 👩‍💻 Author

### Yandapalli Tejaswini

**Computer Science & Engineering (Data Science) Student**

- GitHub: [YandapalliTejaswini](https://github.com/YandapalliTejaswini)

---

## ⭐ Support

If you found this project useful, consider giving the repository a ⭐ **Star**.

