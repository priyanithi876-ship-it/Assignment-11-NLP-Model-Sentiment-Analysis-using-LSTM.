# Customer Review Sentiment Analysis using NLP and LSTM

## 1. Project Overview

This project performs sentiment analysis on customer reviews using Natural Language Processing (NLP) and a Long Short-Term Memory (LSTM) neural network.

The model classifies customer reviews into:

- **0 → Negative Sentiment**
- **1 → Positive Sentiment**

## 2. Objective

The main objectives of this project are:

- Prepare and preprocess text data.
- Tokenize customer reviews.
- Generate numerical sequences from text.
- Apply padding to make sequences equal in length.
- Represent text using Bag of Words, TF-IDF, and Word Embedding.
- Build an LSTM-based sentiment classification model.
- Train and validate the model.
- Generate sentiment predictions.
- Evaluate the model using Accuracy, Precision, Recall, F1 Score, and Confusion Matrix.
- Analyze model performance and limitations.

## 3. Dataset

The project uses the **Keras Built-in IMDB Movie Reviews Dataset**.

Dataset details:

- Total reviews: **50,000**
- Training reviews: **25,000**
- Testing reviews: **25,000**
- Number of classes: **2**
- Label `0`: Negative
- Label `1`: Positive

The dataset contains integer-encoded reviews suitable for NLP and deep-learning experiments.

## 4. Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- NLTK
- Scikit-learn
- TensorFlow
- Keras
- Jupyter Notebook / Google Colab

## 5. Task 1 – Text Data Preparation

The text data preparation process includes:

1. Loading the IMDB dataset.
2. Text cleaning demonstration.
3. Tokenization.
4. Stopword removal demonstration.
5. Word indexing.
6. Sequence generation.
7. Sequence padding.
8. Train-validation splitting.

The maximum sequence length used for the LSTM model is **200**.

## 6. Task 2 – Text Representation

Three text representation techniques are demonstrated:

### Bag of Words

Bag of Words represents text using word-frequency values.

### TF-IDF

TF-IDF gives higher importance to words that are useful for distinguishing documents.

### Word Embedding

The Embedding layer converts word indices into dense numerical vectors. These vectors can learn useful relationships between words during model training.

### Comparison

| Representation | Main Feature |
|---|---|
| Bag of Words | Word frequency |
| TF-IDF | Word importance |
| Word Embedding | Dense semantic representation |

## 7. Task 3 – LSTM Model Development

The LSTM model architecture is:

**Input Text → Embedding Layer → LSTM Layer → Dropout → Dense Layer → Sigmoid Output**

### Model Configuration

- Vocabulary size: **10,000**
- Maximum sequence length: **200**
- Embedding dimension: **128**
- LSTM units: **64**
- Dropout: **0.5**
- Output activation: **Sigmoid**
- Loss function: **Binary Cross-Entropy**
- Optimizer: **Adam**
- Batch size: **64**
- Epochs: **5**

The model is trained using the training data and validated using the validation data.

## 8. Task 4 – Model Evaluation

The trained model is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Classification Report
- Confusion Matrix
- Training vs Validation Accuracy
- Training vs Validation Loss
- Actual vs Predicted Sentiment

The evaluation metrics are calculated from the actual test labels and model predictions.

### Metric Definitions

**Accuracy:** Measures the overall percentage of correct predictions.

**Precision:** Measures how many predicted positive reviews are actually positive.

**Recall:** Measures how many actual positive reviews are correctly identified.

**F1 Score:** Provides a combined measure of precision and recall.

## 9. Task 5 – Performance Analysis

The following aspects are analyzed:

### Impact of Sequence Length

Shorter sequences can reduce computation but may lose important context. Longer sequences can capture more context but require more computation and may contain more padding.

### Importance of Embedding Layer

The Embedding layer converts integer word indices into dense vectors and helps the model learn meaningful word representations.

### LSTM Memory Cells

LSTM memory cells help retain important information from previous words and capture sequential relationships in reviews.

### Overfitting

Overfitting can occur when the model performs much better on training data than validation data.

Possible solutions include:

- Dropout
- Early stopping
- Reducing model complexity
- Increasing training data
- Choosing an appropriate sequence length
- Monitoring validation performance

### Model Limitations

- Very long reviews may require truncation or padding.
- Sarcasm and complex language can be difficult to classify.
- Model performance depends on the quality and type of training data.
- Training an LSTM can require significant computational resources.
- The model may not perform equally well on every type of customer review.

## 10. Training Results

The notebook calculates the actual training and validation performance during execution.

The final evaluation values should be taken directly from the notebook output:

- **Accuracy:** Generated after running Task 4
- **Precision:** Generated after running Task 4
- **Recall:** Generated after running Task 4
- **F1 Score:** Generated after running Task 4

These values should not be manually entered without running the notebook.

## 11. Project Workflow

```text
IMDB Dataset
     ↓
Text Data Preparation
     ↓
Tokenization & Sequence Generation
     ↓
Padding
     ↓
Text Representation
     ↓
Embedding Layer
     ↓
LSTM Model
     ↓
Model Training
     ↓
Sentiment Prediction
     ↓
Model Evaluation
     ↓
Performance Analysis
```

## 12. Expected Output

After successfully running the notebook, the project produces:

- Preprocessed text/sequence information
- Padded sequences
- Bag of Words representation
- TF-IDF representation
- Word Embedding demonstration
- LSTM model summary
- Training and validation results
- Sentiment predictions
- Accuracy
- Precision
- Recall
- F1 Score
- Classification report
- Confusion matrix
- Accuracy graph
- Loss graph
- Actual vs Predicted sentiment visualization
- Performance analysis

## 13. Conclusion

This project demonstrates how NLP and LSTM can be used for customer review sentiment classification.

Traditional text representations such as Bag of Words and TF-IDF provide useful numerical representations of text, while Word Embeddings provide dense representations that can be learned by a deep-learning model.

The LSTM model learns sequential information from review sequences and predicts whether a review belongs to the positive or negative sentiment class.

The evaluation and performance analysis help determine the effectiveness and limitations of the trained sentiment-analysis model.

## 14. Project Structure

```text
Customer-Review-Sentiment-Analysis/
│
├── ASSIGNMENT_11_NLP_MODEL_SENTIMENT_ANALYSIS.IPYNB
├── README.md
│
└── Screenshots/
    ├── task1_output.png
    ├── task2_output.png
    ├── task3_output.png
    ├── task4_output.png
    └── task5_output.png
```

## 15. How to Run

1. Open the `.ipynb` notebook in Google Colab or Jupyter Notebook.
2. Run the cells in order.
3. Complete Task 1 first.
4. Run Task 2.
5. Run Task 3 to train the LSTM model.
6. Run Task 4 to evaluate the model.
7. Run Task 5 to perform performance analysis.
8. Check the generated outputs and graphs.

## 16. Skills Demonstrated

- Natural Language Processing
- Text preprocessing
- Tokenization
- Stopword removal
- Sequence generation
- Padding
- Bag of Words
- TF-IDF
- Word Embedding
- LSTM neural networks
- Binary sentiment classification
- Model evaluation
- Performance analysis
- Data visualization

## 17. Final Status

**Project:** Customer Review Sentiment Analysis using NLP and LSTM

**Tasks Completed:**

- Task 1 – Text Data Preparation ✅
- Task 2 – Text Representation ✅
- Task 3 – LSTM Model Development ✅
- Task 4 – Model Evaluation ✅
- Task 5 – Performance Analysis ✅

**Project Status: Completed**
