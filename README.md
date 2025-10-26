```python
import telebot

# Initialize the bot
bot = telebot.TeleBot("YOUR_TELEGRAM_BOT_TOKEN")

# Define the commands
@bot.message_handler(commands=['start'])
def start(message):
    bot.reply_to(message, "Welcome to the buys bot! Here are the available commands:\n"
                          "/track - Track a specific contract address (CA)\n"
                          "/price - Check current price of a token\n"
                          "/swap - Show recent swaps\n"
                          "/transfers - Show recent transfers\n"
                          "/help - Get help on how to use the bot")

@bot.message_handler(commands=['track'])
def track(message):
    # Add code to track a specific contract address
    bot.reply_to(message, "Tracking contract address...")

@bot.message_handler(commands=['price'])
def price(message):
    # Add code to check current price of a token
    bot.reply_to(message, "Checking current price...")

@bot.message_handler(commands=['swap'])
def swap(message):
    # Add code to show recent swaps
    bot.reply_to(message, "Showing recent swaps...")

@bot.message_handler(commands=['transfers'])
def transfers(message):
    # Add code to show recent transfers
    bot.reply_to(message, "Showing recent transfers...")

@bot.message_handler(commands=['help'])
def help(message):
    bot.reply_to(message, "Here are the available commands:\n"
                          "/track - Track a specific contract address (CA)\n"
                          "/price - Check current price of a token\n"
                          "/swap - Show recent swaps\n"
                          "/transfers - Show recent transfers\n"
                          "/help - Get help on how to use the bot")

# Start the bot
bot.polling()
```
