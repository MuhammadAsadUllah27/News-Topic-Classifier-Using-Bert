
#  News Topic Classifier Using BERT

##  1. Objective of the Task

The objective of this project is to develop an intelligent Natural Language Processing (NLP) system that can automatically classify news headlines into predefined categories such as **World, Sports, Business, and Sci/Tech**.

With the rapid growth of online news content, manual categorization becomes inefficient and time-consuming. This project aims to solve this problem by leveraging a pre-trained transformer model (BERT) to perform accurate and fast text classification.

The key goals include:

* Automating news classification using deep learning
* Utilizing transfer learning with a pre-trained BERT model
* Evaluating model performance using standard metrics
* Deploying the model through an interactive web interface

---

##  2. Methodology / Approach

The project follows a structured machine learning pipeline:

###  Step 1: Dataset Loading

* The **AG News dataset** is loaded using the Hugging Face `datasets` library.
* It contains news headlines categorized into four classes.

###  Step 2: Data Preprocessing & Tokenization

* Text data is tokenized using the BERT tokenizer (`bert-base-uncased`).
* Tokenization converts raw text into numerical tokens suitable for model input.
* Truncation and padding are applied to ensure consistent input length.

###  Step 3: Model Development

* A pre-trained BERT model is loaded for sequence classification.
* The model is configured with:

  * 4 output labels
  * Custom label mappings (id2label and label2id)

###  Step 4: Model Training

* The model is fine-tuned on the AG News dataset using Hugging Face `Trainer`.
* Key training configurations:

  * Learning rate: 2e-5
  * Batch size: 16
  * Epochs: 2
  * Weight decay for regularization
* A subset of data is used for faster experimentation.

###  Step 5: Model Evaluation

* The model is evaluated using:

  * **Accuracy** (overall correctness)
  * **F1-score** (balance between precision and recall)
* Predictions are generated using logits and converted to class labels.

###  Step 6: Deployment

* The trained model is deployed using **Streamlit**.
* A simple user interface allows users to:

  * Input a news headline
  * Receive predicted category instantly

---

##  3. Key Results or Observations

* The BERT model achieved **high accuracy and strong F1-score**, demonstrating effective understanding of text context.
* Even with limited training data (subset), the model performed well due to **transfer learning**.
* The model successfully generalized to unseen headlines and provided correct classifications in most cases.
* Transformer-based models like BERT significantly outperform traditional machine learning methods in NLP tasks.
* Deployment using Streamlit made the model **interactive and user-friendly**, enabling real-time predictions.

###  Observations:

* Increasing training data can further improve performance.
* Fine-tuning hyperparameters (epochs, learning rate) impacts results significantly.
* Tokenization quality plays a crucial role in model accuracy.
* Lightweight deployment tools like Streamlit are effective for showcasing ML projects.

---

##  Conclusion

This project demonstrates a complete end-to-end pipeline for building a modern NLP application using transformers. It highlights the power of BERT in text classification tasks and provides practical experience in data preprocessing, model training, evaluation, and deployment.

---
