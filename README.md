🧠 Breast Cancer Classification using Neural Network
📌 Overview

This project builds a Neural Network model using TensorFlow/Keras to classify breast cancer tumors as Benign (B) or Malignant (M) based on diagnostic features.

The model is trained on a dataset containing 30 numerical features computed from digitized images of breast mass.

📂 Dataset
Total samples: 569
Features: 30 numerical features
Target:
M → Malignant (Cancerous)
B → Benign (Non-cancerous)
⚙️ Workflow
1. Data Preprocessing
Removed unnecessary column: Unnamed: 32
Dropped id column
Encoded labels using LabelEncoder
Split dataset into:
Training set (80%)
Testing set (20%)
Standardized features using StandardScaler
2. Model Architecture

A simple feedforward neural network:

Input layer: 30 features
Hidden layer: 20 neurons (ReLU)
Output layer: 2 neurons (Sigmoid)
3. Training
Optimizer: Adam
Loss: Sparse Categorical Crossentropy
Epochs: 10
Validation Split: 10%
4. Performance
✅ Training Accuracy: ~96%
✅ Validation Accuracy: ~95%
✅ Test Accuracy: 95.6%
5. Visualization
Accuracy vs Epochs
Loss vs Epochs
6. Prediction System

The model can take custom input (30 features) and predict:

0 → Benign
1 → Malignant

Example Output:

Prediction: Malignant
🚀 How It Works
Input data is scaled using the trained scaler
Passed into the trained neural network
Model outputs probabilities
argmax() selects the final class
📊 Tech Stack
Python
NumPy
Pandas
Matplotlib / Seaborn
Scikit-learn
TensorFlow / Keras


You may see this warning:

UserWarning: X does not have valid feature names

This happens because the scaler was trained on a DataFrame but prediction input is a NumPy array.
It does not affect model performance.

💡 Future Improvements
Add Dropout layers to reduce overfitting
Hyperparameter tuning
Deploy using Flask/Streamlit
Use deeper neural networks
