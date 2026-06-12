# Election Comments Analysis Pipeline

Polish & Romanian YouTube Comments Analysis for 2025 Presidential Elections

## Quick Start

1. Install dependencies `pip install -r requirements.txt`
2. Place CSV files in `dataraw` folder
3. Run `00_setup_and_config.ipynb` first
4. Run Polish pipeline (01-06) OR Romanian pipeline (01-06)
5. Optionally run `08_comparative_analysis.ipynb`

## Checkpoint System

Each block saves a `.pkl` checkpoint. If a notebook crashes, re-run it and it will load from the last checkpoint.

## Runtime Estimate

- Full pipeline (both languages) ~2 hours on CPU
- Single language ~60-75 minutes
- Re-run with checkpoints ~10 minutes

## Models Used

- Polish Sentiment `eevvggbert-polish-sentiment-politics`
- Romanian Sentiment `readerbenchro-sentiment`
- Embeddings `sentence-transformersparaphrase-multilingual-MiniLM-L12-v2`
- Topics BERTopic with 8 topics per language
