# Hotel-Booking
# Hotel Booking Cancellation Prediction

## Project Workflow

### 1. Load Dataset
The dataset is loaded using **Pandas**.

---

### 2. Data Exploration (EDA)

The dataset is explored using:

- Dataset shape
- Dataset information
- Statistical summary
- Data types
- Missing values
- Duplicate values
- Histograms
- Count plots
- Correlation Heatmap
- Boxplot

---

### 3. Data Cleaning

The following preprocessing steps are applied:

- Remove invalid bookings (0 adults, 0 children, 0 babies)
- Remove negative ADR values
- Fill missing values
- Remove duplicate rows
- Remove data leakage columns:
  - reservation_status
  - reservation_status_date

---

### 4. Define Target Variable

The target variable is:

**is_canceled**

- 0 → Booking Not Canceled
- 1 → Booking Canceled

---

### 5. Split Dataset

The dataset is divided into:

- Training Set
- Validation Set (for ANN)
- Test Set

---

### 6. Encoding

Categorical features are converted into numerical values using **Label Encoding**.

---

### 7. Feature Scaling

Numerical features are standardized using **StandardScaler**.

---

### 8. Build Classification Models

Three different classification models are created and tested.

---

### 9. Model Training

The following models are trained:

- Logistic Regression
- Random Forest Classifier
- Artificial Neural Network (ANN)

The ANN is trained using:

- Adam Optimizer
- Binary Crossentropy Loss Function
- EarlyStopping

---

### 10. Model Evaluation

Models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix
- Classification Report
- ROC Curve

---

# Models Architecture

## Model 1

### Logistic Regression

- Classification Model
- Max Iterations = 1000

---

## Model 2

### Random Forest

- Number of Trees = 100
- Criterion = Gini Impurity
- Random State = 42

---

## Model 3

### Artificial Neural Network (ANN)

Architecture:

- Input Layer
- Dense Layer (256 Neurons, ReLU)
- Dropout (0.2)
- Dense Layer (128 Neurons, ReLU)
- Dropout (0.2)
- Dense Layer (64 Neurons, ReLU)
- Dropout (0.1)
- Dense Layer (32 Neurons, ReLU)
- Dropout (0.1)
- Output Layer (1 Neuron, Sigmoid)

Optimizer:

- Adam

Loss Function:

- Binary Crossentropy

Callback:

- EarlyStopping

---

# Results

The three models are compared using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

The best model is selected based on the evaluation metrics.

---

# Best Model

The best-performing model is selected according to:

- Highest Accuracy
- Highest ROC-AUC Score

This model provides the most accurate prediction for hotel booking cancellation.

---

# Visualization

The project includes:

- Booking Cancellation Distribution
- Hotel Type Distribution
- Customer Type Distribution
- Market Segment Distribution
- Deposit Type Distribution
- Lead Time Distribution
- ADR Distribution
- Correlation Heatmap
- ADR Boxplot
- Confusion Matrix for each model
- ROC Curve
- ANN Training vs Validation Accuracy
- ANN Training vs Validation Loss
- Model Comparison Bar Chart

These visualizations help analyze the dataset and compare model performance.

---

# Instructions for Running the Project

## Step 1: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow joblib
```

---

## Step 2: Add Dataset

Place the dataset file:

```
hotel_bookings.csv
```

inside the project folder.

---

## Step 3: Run the Project

Run the Jupyter Notebook or Python script.

---

# Output

The project outputs:

- Cleaned dataset
- Trained models
- Evaluation metrics
- Confusion Matrices
- ROC Curves
- ANN Accuracy & Loss graphs
- Model comparison table
- Model comparison chart
- Saved trained models

---

# Saved Models

The project saves:

- logistic_regression.pkl
- random_forest.pkl
- hotel_booking_ann.keras
- scaler.pkl
- label_encoder.pkl

---

# Conclusion

This project demonstrates how Machine Learning and Deep Learning techniques can be used to predict hotel booking cancellations.

Three different classification models were trained and evaluated.

The models were compared using multiple evaluation metrics, and the best-performing model was selected based on its classification performance.
