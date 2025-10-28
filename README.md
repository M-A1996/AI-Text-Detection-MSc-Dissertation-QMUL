# 🧠 AI-Text-Detection-MSc-Dissertation-QMUL

**BERT-based AI text detection system** developed as part of my **MSc Data Science & Artificial Intelligence** dissertation at **Queen Mary University of London**.
This research investigates methods to **distinguish ChatGPT-generated content from human-written text** and explores strategies to **reduce hallucinations** and **enhance interpretability** in generative AI systems.

---

## 🎯 Project Overview

The project aims to address one of the most pressing challenges of the AI era—**identifying machine-generated text** in academic, journalistic, and social contexts. With the growing integration of large language models (LLMs) like ChatGPT, distinguishing human from AI-produced content has become crucial for **academic integrity**, **ethical AI usage**, and **trustworthy information systems**.

Three different model architectures were developed, trained, and compared using the **`aadityaubhat/GPT-wiki-intro` dataset** (150,000+ Wikipedia introductions):

* 🪵 **Random Forest Classifier** — baseline machine-learning model using TF-IDF features.
* 🔁 **LSTM Neural Network** — deep learning model using GloVe embeddings for sequential text processing.
* ⚡ **BERT Transformer** — fine-tuned “bert-base-uncased” model leveraging Hugging Face Transformers.

The BERT-based model outperformed all others, achieving a **test accuracy of 97.5%** and a **perfect ROC-AUC score of 1.00**, demonstrating its robustness in differentiating AI-generated and human-written text.

---

## 🧩 Key Contributions

* Designed and implemented **three NLP pipelines** combining traditional and deep learning techniques.
* Performed **data cleaning, tokenization, augmentation, and balancing** for optimal model generalization.
* Conducted **hyperparameter tuning** and **cross-validation** for performance optimization.
* Integrated **explainability analysis** (feature importance and token saliency) to enhance interpretability.
* Evaluated performance using **Accuracy, ROC-AUC, Precision-Recall, and Confusion Matrices**.
* Delivered a reproducible **Google Colab-based workflow** compatible with CPU/GPU environments.

---

## 🧪 Results Summary

| Model                   | Technique               | Test Accuracy | ROC-AUC  | Training Time | Key Insight                         |
| ----------------------- | ----------------------- | ------------- | -------- | ------------- | ----------------------------------- |
| Random Forest           | TF-IDF Vectorization    | 90.26 %       | 0.97     | 1822 s        | Fast, interpretable baseline        |
| LSTM                    | GloVe Embeddings        | 91.50 %       | 0.97     | 34 s          | Captures sequence dependencies      |
| **BERT (base-uncased)** | Transformer Fine-Tuning | **97.50 %**   | **1.00** | 6916 s        | Best performance and generalization |

---

## ⚙️ Tech Stack

**Languages & Libraries:**
Python 3.10 | PyTorch | TensorFlow/Keras | Hugging Face Transformers | Scikit-learn | NLPAUG | Matplotlib | Pandas | NumPy

**Development Environment:**
Google Colab (A100 GPU) | Jupyter Lab | VS Code

---

## 📊 Dataset Information

**Source:** [`aadityaubhat/GPT-wiki-intro`](https://huggingface.co/datasets/aadityaubhat/GPT-wiki-intro)
**Samples:** ≈ 150 000 paired human-written and GPT-generated Wikipedia introductions
**Preprocessing:** labeling, balancing, tokenization, data augmentation (synonym replacement 20 %)
**Split:** 70 % Training | 15 % Validation | 15 % Testing

---

## 🔍 Explainability & Ethical Considerations

A major focus of this research is **interpretability**.
The project incorporates explainability tools to highlight which linguistic features allow models to distinguish AI-generated text.
This approach promotes **responsible AI**, enabling stakeholders to understand and audit detection outcomes rather than relying on opaque “black-box” predictions.

---

## 📘 Academic Reference

Asghar, M. (2024). *Detection of ChatGPT-Generated Text for Mitigating AI Hallucinations and Improving Interpretability.*
MSc Dissertation, Queen Mary University of London.

---

## 📂 Repository Structure

```
AI-Text-Detection-MSc-Dissertation-QMUL/
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── notebooks/
│   └── MSc_Project_Detection_of_Text_Generated_by_ChatGPT_Final.ipynb
├── report/
│   └── MSc_Project_Dissertation_Research_Paper_Mohammad_Asghar.pdf
└── results/
    ├── confusion_matrices.png
    ├── roc_auc_curves.png
    └── precision_recall_curves.png
```

---

## 🏆 Achievements

* 🎓 Awarded **Distinction** for outstanding performance and research quality.
* 🧠 Demonstrated **97.5 % accuracy / 1.00 ROC-AUC**, surpassing baseline approaches.
* 🤝 Contributed to ongoing discussions on **AI authenticity detection** and **hallucination mitigation**.
* 📈 Built a **fully reproducible** workflow suitable for future LLM-detection extensions (e.g., GPT-4, Claude, Gemini).

