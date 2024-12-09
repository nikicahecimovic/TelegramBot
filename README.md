Here’s an updated README with the code snippet for cloning the repository in a visible box:

# Cryptocurrency Telegram Bot

## Overview
This project is a Telegram bot that provides live cryptocurrency prices and percentage changes over the last 24 hours. The bot interacts with users via the Telegram API and fetches cryptocurrency data from the CoinMarketCap API.

## Features
- Start the bot with a `/start` command.
- Use `/help` to get assistance.
- Type the name of any cryptocurrency to get its current price in USD and the percentage change in the last 24 hours.
- Handles user errors gracefully.
- Fetches live cryptocurrency data using the CoinMarketCap API.

## Prerequisites
Before you start, ensure you have the following installed:
- Python 3.x
- `python-telegram-bot` library
- `requests` library

You also need:
1. A **Telegram Bot Token** from [BotFather](https://core.telegram.org/bots#botfather).
2. A **CoinMarketCap API Key** from [CoinMarketCap](https://coinmarketcap.com/api/).

## Project Structure
- **Constants.py**: Contains API keys (`API_KEY` for Telegram and `API_KEY_COIN` for CoinMarketCap).
- **Currency.py**: Includes functionality to retrieve cryptocurrency data.
- **Responses.py**: Processes and formats user messages for responses.
- **Main Script**: Runs the Telegram bot.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/cryptocurrency-telegram-bot.git
   cd cryptocurrency-telegram-bot

	2.	Install required libraries:

pip install python-telegram-bot requests


	3.	Set up the API keys:
	•	Replace placeholders in Constants.py with your API keys:

API_KEY = 'your-telegram-bot-token'
API_KEY_COIN = 'your-coinmarketcap-api-key'



Usage
	1.	Start the bot:

python main.py


	2.	Interact with the bot on Telegram:
	•	/start: Initiates the bot and displays a welcome message.
	•	/help: Provides basic instructions.
	•	Send the name of any cryptocurrency (e.g., Bitcoin, Ethereum) to get live data.

Functions and Modules

Main Bot Script
	•	start_message: Sends a welcome message when the /start command is issued.
	•	help_message: Provides help instructions when the /help command is issued.
	•	handle_message: Processes user input and provides cryptocurrency data.
	•	error: Logs any errors that occur during bot execution.
	•	main: Sets up and starts the bot.

Currency.py
	•	getCurrency(name): Fetches the price and percentage change for the given cryptocurrency name. Returns a user-friendly message or an error message if the currency is not found.

Responses.py
	•	sample_responses(input_text): Handles user input and calls getCurrency to fetch data.

Example Output
	•	User: Bitcoin
	•	Bot: Current price of Bitcoin is: $34,500.00 USD which is 2.45% higher than yesterday.
	•	User: InvalidCoinName
	•	Bot: Cannot find "InvalidCoinName" in the Cryptocurrencies list, be cautious of typos!

Error Handling

The bot includes robust error handling to log any unexpected issues while interacting with users or fetching data.
