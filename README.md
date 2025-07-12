# Financial Sentiment Analysis with NLP Models

## Overview
This project benchmarks multiple Natural Language Processing (NLP) models for sentiment analysis of financial social media content such as tweets, Reddit posts, and financial news. It also includes a placeholder for sarcasm detection.

## Key Objectives
- Evaluate how different NLP models perform on **financial text**.
- Handle **emojis, tickers, hashtags, and sarcasm**.
- Compare model predictions and highlight strengths and weaknesses.

## Models Used

### 📝 VADER ([GitHub Repo](https://github.com/cjhutto/vaderSentiment))
- Lexicon and rule-based sentiment analysis tool.
- Tuned for **social media language**.
- Outputs: Positive, Neutral, Negative scores + Compound score.
- **Pros:** Fast, no training needed, handles slang/emojis.
- **Cons:** Weak on complex finance language.

### 💰 FinBERT ([Hugging Face](https://huggingface.co/ProsusAI/finbert))
- BERT model fine-tuned on **financial texts**.
- Predicts: Positive, Neutral, Negative.
- **Pros:** Very high accuracy on formal financial documents.
- **Cons:** Less effective for informal social media posts or sarcasm.

### 🔬 DeBERTa ([Hugging Face Docs](https://huggingface.co/docs/transformers/model_doc/deberta))
- General-purpose transformer model with **disentangled attention**.
- Used for sentiment classification without finance-specific tuning.
- **Pros:** Strong contextual understanding, highly accurate.
- **Cons:** Computationally heavier.

### 😏 Sarcasm Detection (Placeholder)
- Uses Hugging Face's `sentiment-analysis` pipeline as a placeholder where sarcasm detection would ideally be integrated in the future.

## Features
- Text preprocessing: emojis, tickers, hashtags.
- Sentiment analysis with multiple models.
- Tabular result comparison.
- Placeholder sarcasm detection.

## Installation
```bash
git clone https://github.com/yourusername/financial-sentiment-analysis.git
cd financial-sentiment-analysis
pip install -r requirements.txt
```

## Usage
```bash
jupyter notebook Sentiment_Analysis.ipynb
```

## Example Output
| Model   | Sentiment         | Probabilities                  |
|---------|-------------------|---------------------------------|
| VADER   | Compound Score     | {'neg': 0.0, 'neu': 0.5, 'pos': 0.5, 'compound': 0.77} |
| FinBERT | Positive           | [0.05, 0.03, 0.92]             |
| DeBERTa | Positive           | [0.12, 0.10, 0.78]             |

## Key Takeaways
| Model     | Strengths                          | Weaknesses                          |
|----------|-------------------------------------|--------------------------------------|
| **VADER**   | Fast, easy, emoji/slang-aware         | Weak on context, sarcasm, complex text |
| **FinBERT** | Finance-specific accuracy             | Less effective on social media        |
| **DeBERTa** | Strong general understanding          | Needs more compute                   |
| **Sarcasm** | Placeholder for future detection      | Not yet implemented                  |


