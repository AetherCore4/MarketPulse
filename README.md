# 📊 MarketPulse — AI Stock Impact Analyzer

MarketPulse is an AI-powered web application that converts financial news into structured, actionable stock insights using Google’s Gemini API.

It acts like a digital analyst — reading news, decoding sentiment, and translating it into market impact signals in seconds.

---

## 🚀 Features

* 🤖 **AI-Driven Analysis**
  Uses Gemini AI to interpret financial news with contextual understanding

* 📈 **Stock Impact Evaluation**
  Identifies how news affects stock price, sentiment, and company outlook

* 🧾 **Structured Output (JSON)**
  Clean, machine-readable format for seamless frontend rendering

* 🔍 **Detailed Insights Extraction**

  * Company Name & Ticker
  * Market Summary
  * Investor Sentiment
  * Impact Magnitude (Low / Medium / High)
  * Financial Metrics Affected
  * Short-term Reaction
  * Long-term Outlook
  * Risk Factors
  * Industry / Peer Impact
  * Financial Terminology Explained

* ⚡ **Fast & Responsive UI**
  Smooth frontend with real-time feedback

* 🛡️ **Error Handling**
  Handles API failures, invalid input, and missing keys gracefully

---

## 🧠 How It Works

### 🔹 Backend (Flask API)

* Accepts news input via `/analyze` endpoint
* Sends structured prompt to Gemini API
* Processes and cleans response
* Returns formatted JSON

### 🔹 Frontend (HTML + JS)

* User inputs news
* Sends request to backend
* Displays structured analysis
* Shows loading state during processing

---

## 📁 Project Structure

```
.
├── app.py
├── requirements.txt
├── .env              # (ignored)
├── .env.example      # template
└── templates/
    └── index.html
```

---

## ⚙️ Setup & Installation

### 🔧 Prerequisites

* Python 3.7+
* Gemini API Key

---

### 🚀 Steps

#### 1. Clone Repository

```bash
git clone https://github.com/AetherCore4/MarketPulse.git
cd MarketPulse
```

#### 2. Install Dependencies

```bash
pip install Flask Flask-Cors python-dotenv requests
```

#### 3. Setup Environment Variables

Create a `.env` file:

```env
GEMINI_API_KEY=your_actual_api_key
```

⚠️ Never upload `.env` to GitHub

---

#### 4. Create `.env.example` (Recommended)

```env
GEMINI_API_KEY=your_api_key_here
```

---

#### 5. Run the Application

```bash
python app.py
```

Open in browser:

```
http://localhost:8080
```

---

## 🧪 Usage

1. Paste financial/news content
2. Click **Analyze**
3. View structured stock insights instantly

---

## 🔐 Environment Variables

| Variable       | Description         |
| -------------- | ------------------- |
| GEMINI_API_KEY | Your Gemini API Key |

---

## 🛠 Tech Stack

* **Backend:** Python, Flask
* **Frontend:** HTML, CSS, JavaScript
* **AI:** Google Gemini API
* **Libraries:** requests, python-dotenv

---

## 📌 Future Enhancements

* 📊 Real-time stock price integration
* 🧠 Multi-news aggregation
* 📉 Sentiment trend graphs
* ☁️ Deployment (Render / Vercel / AWS)
* 🔔 Alert system for stock-impacting news

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a Pull Request

---

## 📜 License

MIT License

Copyright (c) 2026 Jishan Shaikh

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files...

---

## 🌟 Support

If you like this project, consider giving it a ⭐ on GitHub
It helps others discover it and keeps the momentum alive 🚀

---

## 💡 Inspiration

MarketPulse is inspired by how modern traders rely on fast, AI-powered insights instead of manually analyzing news.

Think of it as your **personal AI financial analyst** — always reading, always interpreting.
