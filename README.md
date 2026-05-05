# StockSage 📈

StockSage is a sophisticated, AI-driven stock market analysis and prediction engine. It combines real-time financial data, advanced technical indicators, and cutting-edge Large Language Models (LLMs) to provide actionable insights for both NSE and BSE stocks.

## 🚀 Key Features

- **AI-Powered Stock Analysis**: Deep dive into any stock with **Google Gemini 2.0 Flash**. Get clear BUY/SELL signals, trading levels, and a structured summary of pros and cons.
- **Sentiment Engine**: Multi-model sentiment analysis using **Groq (Llama 3)** and **Perplexity AI** to gauge market mood from news headlines.
- **Real-time Data Streaming**: Hybrid data fetching logic using `yfinance` and real-time scraping from Google Finance for accurate, up-to-the-minute pricing.
- **Comprehensive Financials**: Access revenue, net income, assets, liabilities, and net worth data, all formatted in INR Crores for easy interpretation.
- **Corporate Intelligence**: Track corporate announcements, stock splits, dividends, and quarterly/annual results.
- **Interactive Visualizations**: High-performance charts using **Recharts** with support for multiple timeframes (1D, 1W, 1M, 6M, 1Y, 5Y, MAX).
- **Market Movers**: Stay updated with real-time Top Gainers and Top Losers from the NSE.
- **News Integration**: Global and local news aggregation via **Marketaux** and **SerpApi**.

## 🛠️ Tech Stack

### Backend (The Brain)
- **Framework**: Django & Django REST Framework (DRF)
- **AI/LLM**: Google Generative AI (Gemini), Groq SDK, Perplexity API
- **Data Analysis**: Pandas, NumPy, Scikit-learn, XGBoost
- **Market Connectors**: yfinance, jugaad-data (NSE Live), nsetools
- **Technical Analysis**: TA-Lib, pandas_ta

### Frontend (The Interface)
- **Library**: React.js 19
- **Design System**: Material UI (MUI) & Chakra UI
- **Animations**: Framer Motion
- **Charting**: Recharts
- **Styling**: Emotion, CSS3 (Modern Glassmorphism)

## 📦 Quick Start

### Prerequisites
- Python 3.10+
- Node.js 18+

### 1. Clone & Install Backend
```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

### 2. Clone & Install Frontend
```bash
cd frontend
npm install
npm start
```

## 🔑 Security & Environment Variables

Create a `.env` file in the `backend` directory. StockSage requires the following keys to function at full capacity:

```env
# AI Models
GEMINI_API_KEY=your_google_gemini_key
GROQ_API_KEY=your_groq_key
PERPLEXITY_API_KEY=your_perplexity_key

# News & Search APIs
MARKETAUX_API_TOKEN=your_marketaux_token
SERPAPI_KEY=your_serpapi_key
```

## 📱 Mobile Support
StockSage is mobile-ready via **Capacitor**. To sync with Android:
```bash
cd frontend
npx cap sync android
npx cap open android
```

## 📄 License
MIT License - Copyright (c) 2026 Airzac LLC
