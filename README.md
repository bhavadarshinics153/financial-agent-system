# 💰 AI Financial Request Prioritizer

Automated financial request prioritization using Groq LLM + custom scoring.

## Features

✅ Multi-currency (USD, EUR, INR, ZAR, IDR)  
✅ AI urgency detection with reasons  
✅ Priority scoring (urgency + amount + timeline)  
✅ Web interface - upload CSV → download output  
✅ Bulk processing  

## Quick Start

```bash
pip install flask pandas groq
$env:GROQ_API_KEY="your_key"
python app.py
```

Open: `http://localhost:5000`

## How It Works

1. Upload `requests.csv`
2. AI detects currency, urgency, reason
3. Calculates priority score
4. Download `output.csv`

## Scoring

- **Urgency:** High=50, Medium=30, Low=10
- **Amount (USD):** >$10K=30, >$5K=20, >$1K=10, else=5
- **Timeline:** ≤7d=20, ≤30d=15, ≤90d=10, else=5

**Categories:** High≥70, Medium≥40, Low<40

## Built With

Flask + Groq LLM

## License

MIT
