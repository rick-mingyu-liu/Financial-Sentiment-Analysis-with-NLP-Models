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

## Future Work
- Integrate a robust sarcasm detection model.
- Add more financial-specific datasets.
- Deploy as a web-based sentiment analysis tool.
