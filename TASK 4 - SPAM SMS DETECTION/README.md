# Spam Detection using Naive Bayes

This project implements a Spam Detection system using the Naive Bayes algorithm. It processes SMS text messages and predicts whether the message is "Ham" (not spam) or "Spam". The model is trained using Term Frequency-Inverse Document Frequency (TF-IDF) as a feature extraction method.

## Dataset

The dataset used is a CSV file containing SMS messages labeled as either "ham" or "spam". The dataset is preprocessed, and features are extracted for the model.

## Project Structure

1. **Data Loading**: 
   - Loaded a CSV file containing SMS messages and their labels.
   - Dropped unnecessary columns and renamed the columns to 'label' and 'sms'.

2. **Data Preprocessing**:
   - Converted labels into binary form: 'ham' (0) and 'spam' (1).
   - Cleaned the text messages by converting to lowercase and removing punctuation (numbers are retained).
   - Added a feature for message length to explore its impact on spam detection.

3. **Feature Engineering**:
   - Used TF-IDF (Term Frequency-Inverse Document Frequency) to extract text features from SMS messages.
   - Balanced the dataset using the RandomOverSampler from the imbalanced-learn library to address class imbalance.

4. **Model Building**:
   - A **Naive Bayes (MultinomialNB)** classifier is used to classify the SMS messages as spam or ham.

5. **Model Evaluation**:
   - Accuracy, confusion matrix, and classification report are generated to assess the model performance.
   - AUC-ROC curve is plotted to evaluate the model's classification ability.

## Installation

### Prerequisites:
- Python 3.10.12

### Steps:
1. Clone the repository:
    ```bash
    git clone <repository-url>
    ```
2. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the Python script to train the model and evaluate its performance.

## Dependencies

- **Pandas**: For data manipulation and analysis.
- **Numpy**: For numerical operations.
- **Seaborn** and **Matplotlib**: For visualizations.
- **Scikit-learn**: For machine learning algorithms and metrics.
- **Imbalanced-learn**: For handling imbalanced datasets.
- **TF-IDF Vectorizer**: For text feature extraction.

## Results

The project evaluates the Naive Bayes model using:
- **Confusion Matrix**
- **Accuracy Score**
- **Classification Report** (Precision, Recall, F1-Score)
- **ROC-AUC Score**

Visualization of the model's performance includes:
- Confusion Matrix Heatmap
- ROC-AUC Curve

## Usage

1. Load the dataset and preprocess the text data.
2. Extract features using TF-IDF.
3. Train the Naive Bayes classifier.
4. Evaluate the model performance.
