# 🎓 Homework Assistant Bot

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Telegram](https://img.shields.io/badge/Telegram-Bot-blue.svg)](https://core.telegram.org/bots)

> **Your personal homework tracking companion** 📚

A smart Telegram bot that monitors your homework submissions on Yandex Practicum and keeps you updated on their review status in real-time.

## ✨ Features

- 🔄 **Automatic Monitoring**: Checks homework status every 10 minutes
- 📱 **Instant Notifications**: Sends Telegram messages when status changes
- 📊 **Status Tracking**: Monitors three key states:
  - `reviewing` - Work is under review
  - `approved` - Work passed review! 🎉
  - `rejected` - Work needs revisions
- 🛡️ **Error Handling**: Robust error handling with detailed logging
- 🔐 **Secure**: Uses environment variables for sensitive tokens

## 🚀 How It Works

1. **Continuous Monitoring**: The bot polls the Yandex Practicum API every 10 minutes
2. **Status Analysis**: Analyzes API responses for homework status changes
3. **Smart Notifications**: Sends relevant Telegram messages only when status changes
4. **Comprehensive Logging**: Logs all activities and sends error alerts to Telegram

## 🛠️ Technologies

- **Python 3.8+** - Core programming language
- **python-telegram-bot 13.7** - Telegram Bot API integration
- **requests 2.26.0** - HTTP library for API calls
- **python-dotenv 0.19.0** - Environment variable management
- **pytest 6.2.5** - Testing framework

## 📋 Prerequisites

Before running this bot, you'll need:

- Python 3.8 or higher
- A Yandex Practicum account with API access
- A Telegram bot token (get from [@BotFather](https://t.me/botfather))
- Your Telegram chat ID

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd Assistant_bot
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   Create a `.env` file in the project root:
   ```env
   PRACTICUM_TOKEN=your_practicum_api_token
   TELEGRAM_TOKEN=your_telegram_bot_token
   TELEGRAM_CHAT_ID=your_telegram_chat_id
   ```

## 🎯 Usage

Run the bot with:
```bash
python homework.py
```

The bot will:
- Validate all required environment variables
- Start monitoring your homework status
- Send notifications to your Telegram chat
- Log all activities to console

## 🧪 Testing

Run the test suite:
```bash
pytest
```

The project includes comprehensive tests covering:
- API response handling
- Telegram message sending
- Error scenarios
- Token validation
- Status parsing

## 📁 Project Structure

```
Assistant_bot/
├── homework.py          # Main bot logic
├── requirements.txt     # Python dependencies
├── README.md           # This file
├── tests/              # Test suite
│   ├── test_bot.py     # Main test file
│   ├── conftest.py     # Test configuration
│   └── fixtures/       # Test data
└── Procfile            # Deployment configuration
```

## 🔧 Configuration

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `PRACTICUM_TOKEN` | Your Yandex Practicum API token | ✅ |
| `TELEGRAM_TOKEN` | Your Telegram bot token | ✅ |
| `TELEGRAM_CHAT_ID` | Your Telegram chat ID | ✅ |

### Customization

You can modify the following constants in `homework.py`:
- `RETRY_TIME`: Polling interval (default: 600 seconds)
- `ENDPOINT`: API endpoint URL
- `HOMEWORK_STATUSES`: Custom status messages

## 🚨 Error Handling

The bot includes comprehensive error handling:
- **API Failures**: Logs and reports API errors
- **Network Issues**: Handles connection timeouts
- **Missing Tokens**: Validates environment variables on startup
- **Invalid Responses**: Validates API response structure

## 📝 Logging

The bot provides detailed logging:
- **Info Level**: Successful operations and status updates
- **Error Level**: API errors and exceptions
- **Debug Level**: Detailed debugging information
- **Critical Level**: Missing environment variables

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- Yandex Practicum for providing the API
- Telegram for the bot platform
- The Python community for excellent libraries

---

**Made with ❤️ for students who want to stay on top of their homework!**