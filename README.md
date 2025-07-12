# Financial Sentiment Analysis with NLP Models

## Overview
This project benchmarks multiple Natural Language Processing (NLP) models for sentiment analysis of financial social media content such as tweets, Reddit posts, and financial news. It also includes a placeholder for sarcasm detection.

## Models Used
- **VADER:** Lexicon and rule-based sentiment analysis tool.
- **FinBERT:** BERT model fine-tuned on financial texts.
- **DeBERTa:** General-purpose transformer model for text classification.
- **Sarcasm Detection:** Placeholder using Hugging Face's sentiment-analysis pipeline.

## Features
- Preprocessing for financial text (emojis, tickers, hashtags).
- Sentiment prediction using multiple models.
- Comparison of model outputs in tabular form.
- Placeholder sarcasm detection.

## Installation
1. Clone the repository:
```bash
git clone https://github.com/yourusername/financial-sentiment-analysis.git
cd financial-sentiment-analysis
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

## Usage
Run the Jupyter notebook to execute:
```bash
jupyter notebook Sentiment_Analysis.ipynb
```

## Example Output
| Model   | Sentiment         | Probabilities                  |
|---------|-------------------|---------------------------------|
| VADER   | Compound Score     | {'neg': 0.0, 'neu': 0.5, 'pos': 0.5, 'compound': 0.77} |
| FinBERT | Positive           | [0.05, 0.03, 0.92]             |
| DeBERTa | Positive           | [0.12, 0.10, 0.78]             |

FinBERT - https://huggingface.co/ProsusAI/finbert

- A pre-trained NLP model specifically designed to analyze the sentiment of **financial text**, such as earnings reports, analyst commentary, and market news.
- Key Features:
    - Achieve 98-99% accuracy and F1 scores in financial phrase benchmarks
    - Supports **positive**, **negative**, and **neutral** sentiment labels.
    - Fine-tuned on the **Financial PhraseBank** dataset.
- Pros:
    - Excellent performance on **formal financial language** (e.g., news articles, reports).
- Cons:
    - Not optimized for **social media slang**, emojis, sarcasm, or informal finance discussions (e.g., Reddit, Twitter).

VADER - https://github.com/cjhutto/vaderSentiment

- A **lexicon and rule-based** sentiment analysis tool specifically tuned for **social media text**, including microblogs and online reviews.
- Key Features:
    - Fast and lightweight — no model training required.
    - Understands **capitalization, slang, emojis, emoticons**.
    - Outputs both **polarity scores (pos, neu, neg)** and a **compound score** (overall sentiment).
- Pros:
    - Easiest to implement
    - Works reasonably well for **short texts** like tweets, headlines, Reddit posts.
- Cons:
    - Lower accuracy on **complex financial language** or multi-sentence inputs.

DeBERTa - https://huggingface.co/docs/transformers/model_doc/deberta

- A cutting-edge **transformer-based model** that improves upon BERT and RoBERTa by using **disentangled attention** and **enhanced decoding**
    - BERT = Bidirectional Encoder Representations from Transformers
        - Developed by Google
        - Pros:
            - Powerful **contextual understanding** (better than traditional word embeddings like Word2Vec or GloVe).
        - Cons:
            - Computationally heavy
    - **RoBERTa** = **Robustly Optimized BERT Approach**
        - Developed by Facebook AI
        - Pros:
            - Strong general-purpose model.
        - Cons:
            - Still requires **GPU resources**.
- Key Features:
    - Outperforms traditional BERT models on various NLP benchmarks.
    - Available pretrained checkpoints (base, large, v2, v3).
    - Easily accessible via **Hugging Face Transformers** with full PyTorch and TensorFlow support.
- Pros:
    - Highly effective for both **document-level** and **aspect-based** sentiment analysis.
    - Supports **fine-tuning** for domain-specific tasks (finance, healthcare, etc.).
- Cons:
    - Requires more **computational resources** (CPU/GPU).
