# 🤖 Twitter Bot

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Twitter](https://img.shields.io/badge/Twitter-API-1DA1F2?logo=twitter&logoColor=white)
![Tweepy](https://img.shields.io/badge/Tweepy-3.10-orange)
![License](https://img.shields.io/badge/License-MIT-green)

A collection of Twitter automation scripts built with Tweepy. The bot can auto-retweet a user's liked tweets, post status updates, and test API connectivity — all configured via `.env` environment variables.

## ✨ Features

- 🔁 **Auto-Retweet Likes** — Fetches a user's liked tweets and retweets them automatically
- 🧩 **Modular Design** — Shared auth and retweet logic in `services.py`
- 🔐 **Environment-Based Config** — All credentials loaded from a `.env` file (no hardcoded keys)
- 🧪 **Test Script** — Quickly verify API connectivity with a "Hello, World!" tweet

## 🛠 Tech Stack

| Layer    | Technology         |
|----------|--------------------|
| Language | Python 3.x         |
| Twitter  | Twitter API v1.1   |
| Library  | Tweepy 3.10        |
| Config   | python-dotenv      |

## 📦 Installation

```bash
git clone https://github.com/Fahad-BA/twitter-bot.git
cd twitter-bot
pip install -r requirements.txt
```

## ⚙️ Configuration

Create a `.env` file in the project root:

```env
API_KEY=your_consumer_key
API_SECRET=your_consumer_secret
ACCESS_TOKEN=your_access_token
ACCESS_SECRET=your_access_token_secret
```

### Getting the keys

1. Apply for a [Twitter Developer account](https://developer.twitter.com/)
2. Create an app and generate your **Consumer Keys** and **Access Tokens**
3. Make sure the app has **Read and Write** permissions

## 🚀 Usage

### Auto-retweet a user's likes

```bash
python retweet_bot.py
```

This authenticates via `services.py`, fetches liked tweets from the configured user, and retweets them.

### Post a test tweet

```bash
python tweepy_test.py
```

Posts a "Hello, World!" status update to verify API connectivity.

### List liked tweet IDs

```bash
python likes.py
```

Fetches and prints the IDs of the 5 most recent liked tweets.

## 📁 Project Structure

```
twitter-bot/
├── retweet_bot.py   # Main script — retweets a user's likes
├── retweets.py      # Standalone retweet logic
├── likes.py         # Fetches and prints liked tweet IDs
├── services.py      # Shared auth + retweet helper functions
├── tweepy_test.py   # Quick API connectivity test
├── requirements.txt # Python dependencies
└── .env             # Your credentials (not committed)
```

## 📄 License

This project is licensed under the MIT License.
