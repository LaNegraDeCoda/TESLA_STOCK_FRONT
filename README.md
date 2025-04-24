# TESLA_STOCK_FRONT
Simple TESLA API Frontend

# ⚡ TESLA Stock Viewer (Frontend Only - 5 Min Intraday)

This is a simple, lightweight web app that fetches **real-time Tesla (TSLA)** stock prices using the **Alpha Vantage API** — specifically the **Intraday (5-minute interval)** data feed.

> ❗️This version is for educational/demo purposes only. The API key is **hardcoded in the frontend**, which is **not secure for production** For this code to work YOU WILL NEED AN API KEY.

---

## 🚀 What It Does

- ✅ Fetches TSLA stock prices every 5 minutes (intraday data)
- ✅ Displays raw JSON response in a readable format
- ❌ No charts
- ❌ No backend
- ❌ No security for API key (visible in browser dev tools)

---

## 📦 Project Structure

TESLA_STOCK_FRONT/ ├── index.html # The only file you need — everything is in here! └── README.md # You're reading it

---

## 🔑 Where the API Comes From

The app uses the free [Alpha Vantage API](https://www.alphavantage.co/documentation/):

- API Endpoint: `https://www.alphavantage.co/query`
- Function used: `TIME_SERIES_INTRADAY`
- Symbol: `TSLA`
- Interval: `5min`
- API Key: `"demo"` (the official Alpha Vantage demo key)

### 📄 Sample URL

```txt
https://www.alphavantage.co/query?function=TIME_SERIES_INTRADAY&symbol=TSLA&interval=5min&apikey=demo
🔗 You can replace the "demo" key with your own free API key from Alpha Vantage.

🧪 How To Use
Clone or download this repo.

Open index.html in your browser.

Select the "Intraday (5min)" option and click "Fetch Data".

View the returned stock data in raw JSON format.

git clone https://github.com/LaNegraDeCoda/TESLA_STOCK_FRONT.git
cd TESLA_STOCK_FRONT
open index.html

✅ You’ll see something like:

{
  "Meta Data": {
    "1. Information": "Intraday (5min) open, high, low, close prices and volume",
    ...
  },
  "Time Series (5min)": {
    "2025-04-23 14:40:00": {
      "1. open": "162.4600",
      "2. high": "162.5700",
      "3. low": "161.9300",
      "4. close": "162.3000",
      "5. volume": "2454320"
    },
    ...
  }
}
⚠️ Why This Is NOT Secure
In this version:

The API key is visible in the frontend JavaScript

Anyone can inspect your code and copy your API key

This could lead to rate limits or unauthorized usage under your account

For secure and production-ready development, use a Node.js backend + .env file to hide your API key.

👉 See the backend-secure version here: TSLA_STOCK_BACKEND (coming soon)

🛠 Tech Stack
HTML5

Vanilla JavaScript (ES6)

Alpha Vantage API

👩🏾‍💻 Author
Made with love by
@LaNegraDeCoda
MIND YOUR TECH IN BUSINESS.

📜 License
MIT — Open to learn, remix, and explore!
