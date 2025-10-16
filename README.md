# Sentiment Classification on IMDB using ModernBERT

### 🧠 Overview
This project fine-tunes **ModernBERT** on the [IMDB movie reviews dataset](https://ai.stanford.edu/~amaas/data/sentiment/) to perform **binary sentiment classification** (positive / negative).  
The goal is to evaluate ModernBERT’s general-domain performance and compare it to traditional BERT-based sentiment models.

### 📊 Dataset
- **Source:** IMDB Large Movie Review Dataset  
- **Samples:** 50,000 labeled reviews (42.5k train / 3.75k test / 3.75k val)  
- **Task:** Binary classification — *positive* vs. *negative* sentiment

### 💻 Method
- **Model:** `answerdotai/ModernBERT-base` (pre-trained)
- **Tokenizer:** `AutoTokenizer.from_pretrained("answerdotai/ModernBERT-base")`
- **Fine-tuning:** Hugging Face `Trainer`
  - Learning rate: `5e-5`
  - Batch size: `8`
  - Early stopping based on validation loss
- **Loss:** CrossEntropyLoss
- **Metrics:** Accuracy, F1-score

### 🚀 Results
| Metric | Score |
|--------|--------|
| Accuracy | 92.8% |
| F1-score | 92.6% |

> ModernBERT achieved strong generalization on the IMDB dataset, confirming its efficiency and robustness on general-domain sentiment classification tasks.
