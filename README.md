
#  Auto Tagging Support Tickets Using LLM

---

##  Objective of the Task

The objective of this project is to automatically classify free-text customer support tickets into predefined categories using Large Language Models (LLMs) and machine learning techniques.

The system is designed to:

* Automatically assign relevant tags to support tickets
* Output the **top 3 most probable categories** for each ticket
* Compare different approaches including zero-shot prompting, few-shot prompting, and a fine-tuned classifier
* Evaluate model performance using Top-1 and Top-3 accuracy metrics

---

##  Methodology / Approach

This project follows a multi-stage NLP pipeline:

### 1. Dataset Preparation

* A synthetic dataset of support tickets was generated
* Each ticket was mapped to one of 10 predefined categories
* Categories include payment, refund, login issues, technical bugs, and more

---

### 2. Zero-Shot Learning (LLM Prompting)

* The model was given only instructions and label categories
* No examples were provided
* Used as a baseline approach for classification

---

### 3. Few-Shot Learning (Prompt Engineering)

* A few labeled examples were included in the prompt
* The model learned patterns from examples using in-context learning
* Improved classification performance compared to zero-shot

---

### 4. Fine-Tuned Machine Learning Model

* TF-IDF was used to convert text into numerical features
* Logistic Regression was trained on labeled dataset
* Model directly learned mapping between tickets and categories

---

### 5. Evaluation Strategy

All models were evaluated using:

* Top-1 Accuracy
* Top-3 Accuracy (whether correct label appears in top 3 predictions)

---

##  Key Results / Observations

* Zero-shot prompting showed the weakest performance due to lack of examples
* Few-shot prompting improved accuracy by providing contextual guidance
* The fine-tuned model achieved the highest performance due to supervised learning on structured data
* Top-3 evaluation provided a more realistic measure of model performance compared to Top-1 alone

---

##  Summary of Results

| Method           | Top-1 Accuracy                     | Top-3 Accuracy        |
| ---------------- | ---------------------------------- | --------------------- |
| Zero-Shot        | Low (~0.10–0.15)                   | Very Low              |
| Few-Shot         | Moderate (~0.20–0.35)              | Improved (~0.25–0.40) |
| Fine-Tuned Model | High (up to 1.0 on synthetic data) | High (up to 1.0)      |

---

##  Conclusion

This project demonstrates how different natural language processing approaches evolve from simple prompting techniques to fully trained machine learning models. It highlights the effectiveness of prompt engineering and supervised learning for support ticket classification.

