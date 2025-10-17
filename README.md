# Sentiment Analysis Twitter — Gender Equality & SDG 5 Focus

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)  
[![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)]()

##  Project Overview

This repository extends the original **Sentiment Analysis Twitter** codebase to specifically address **SDG 5: Gender Equality** by harvesting and analyzing Twitter data around gender issues (e.g. women’s rights, gender-based violence, equality in employment/education) and extracting insights from public sentiment.

Key goals:

- Collect tweets centered on gender equality, women’s rights, gender-based violence, representation in STEM, etc.  
- Clean, preprocess, and classify sentiment (positive, negative, neutral) with respect to gender topics.  
- Explore trends over time, geographic/demographic differences, and correlations with gender equality indicators.  
- Provide visualizations, dashboards, and reports to support advocacy, policy, or academic work.  

##  Repository Structure

```
.
├── data/
│   ├── raw/             ← raw tweet JSON / CSV dumps
│   ├── processed/       ← cleaned & preprocessed data
│   └── metadata/        ← auxiliary files (e.g. hashtag lists, keyword lists)
├── notebooks/
│   ├── Sentiment‑Analysis‑Twitter.ipynb
│   └── EDA_gender_insights.ipynb
├── src/
│   ├── scraper.py       ← tweet collection (via Twitter API)
│   ├── preprocess.py    ← cleaning, tokenization, stopword removal
│   ├── sentiment_model.py ← model training / prediction
│   ├── analysis.py       ← statistics, trend detection
│   └── visualization.py  ← plotting, dashboards
├── requirements.txt
├── LICENSE
└── README.md
```

## 🛠 Setup & Installation

1. **Clone repository**  
   ```bash
   git clone https://github.com/YourUsername/Sentiment‑Analysis‑Twitter.git
   cd Sentiment‑Analysis‑Twitter
   ```

2. **Create & activate virtual environment**  
   ```bash
   python3 -m venv venv
   source venv/bin/activate     # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up Twitter API credentials**  
   - You’ll need a Twitter Developer account and bearer token (or API keys).  
   - Export these as environment variables, e.g.:  
     ```bash
     export TWITTER_BEARER_TOKEN="your_token_here"
     ```
   - Alternatively, create a config file (e.g. `config.yaml` or `.env`) with your credentials (ensure it is added to `.gitignore`).

5. **Run data collection**  
   - Use `scraper.py` or a notebook to fetch tweets matching your gender equality search queries (hashtags, keywords).

6. **Preprocess & train**  
   ```bash
   python src/preprocess.py --input data/raw/... --output data/processed/...
   python src/sentiment_model.py --train data/processed/train.csv --model_out models/
   ```

7. **Analyze & visualize**  
   ```bash
   python src/analysis.py --input data/processed/...
   python src/visualization.py --input results/... --out figs/
   ```

##  Connecting to SDG 5 (Gender Equality)

This project aligns with **SDG 5** in the following ways:

- By analyzing how social media discourse around gender evolves, it surfaces public sentiment, concerns, and attitudes.
- Identifies hotspots of negative sentiment or controversies (e.g. backlash against policy changes, gender violence cases).
- Supports advocacy groups, policymakers, researchers with data-driven evidence.
- Helps track progress or regression in public attitudes over time or across regions.

##  Possible Extensions

- **Multilingual support** — handle tweets in multiple languages (English, Swahili, French, etc.).  
- **Aspect‑based sentiment** — differentiate sentiment toward specific gender topics (e.g. education, workplace, violence).  
- **Geospatial analysis** — map sentiment by country, region, city.  
- **Time-series anomaly detection** — detect sudden shifts in sentiment associated with events (e.g. policy change, viral campaign).  
- **Dashboard / Web UI** — interactive dashboards (e.g. via Dash, Streamlit, or Flask) for non‑technical users.  
- **Deep learning models** — try transformer models (e.g. BERT, RoBERTa) fine‑tuned for gender discourse.

##  Contributing

We welcome contributions, especially around:

- Improving data collection for gender topics  
- Better preprocessing (e.g. more advanced noise removal)  
- Model improvements, transfer learning or fine‑tuning  
- Visualization, dashboards, and dissemination  
- Adding real case studies (e.g. particular countries, events)

If you propose changes, please create a pull request and include tests where applicable.

##  License & Credits

This project is licensed under the **MIT License** (see `LICENSE`).  
Original base repository and notebook code come from **Ruturajnikm / Sentiment‑Analysis‑Twitter**.  
Please acknowledge any reused portions and give credit in your work.

