Epileptic Seizure Detection using CNN
Dataset: "https://www.kaggle.com/datasets/harunshimanto/epileptic-seizure-recognition#Epileptic%20Seizure%20Recognition.csv"

Based on the Epileptic Seizure Recognition Dataset from Kaggle.
Contains 11,500 samples with 178 EEG signal features per sample.
Labels are binarized: 1 for seizure events and 0 for non-seizure events.

Preprocessing:

Unnecessary columns are dropped.
The target variable (y) is converted into binary labels.
Data is reshaped appropriately for a 1D CNN.
Dataset is split into 80% training and 20% testing sets.

Model Architecture:

Utilizes a 1D Convolutional Neural Network (CNN) to capture temporal patterns in EEG signals.
Layers:
Conv1D Layers: To extract local features.
MaxPooling1D Layers: To reduce dimensionality and noise.
Flatten Layer: To convert the 2D output into a 1D feature vector.
Dense Layers: For final classification.
Dropout Layer: To prevent overfitting.
Uses a sigmoid activation function in the final layer for binary classification.

Training & Evaluation:

Model is compiled with the Adam optimizer and binary cross-entropy loss.
Trained over 20 epochs with a batch size of 32.
Evaluation Metrics:
Accuracy: Approximately 87% on the test set.
R² Score: Around 0.81.
Confusion Matrix, Classification Report (Precision, Recall, F1-score): Provided for detailed performance analysis.
Outcome:

The CNN model demonstrates promising performance in detecting epileptic seizures from EEG data.
The results indicate that deep learning approaches can effectively capture the underlying patterns in EEG signals for seizure prediction.
