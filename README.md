Telegram Bot to Ban Non-Bot Members

This Python script uses the Pyrogram library to create a Telegram bot that automatically bans non-bot members from any group it is added to. It logs removed users to a file (remove.txt) and ensures robust error handling, proper logging, and configuration flexibility.

---

Features:
- Automatically bans non-bot members: Any member who is not a bot will be banned upon the receipt of a message.
- Logs removed members: The ID and username (if available) of each banned user are logged in a text file remove.txt.
- Customizable configuration: Easily set up and change bot parameters.
- Error handling and logging: All actions, errors, and exceptions are logged using Python’s built-in logging module.

---

Requirements:
- Python 3.7+
- Pyrogram library
- Telegram bot created via BotFather
- api_id, api_hash, and bot_token from Telegram

---

Installation:

1. Clone the Repository

   First, clone this repository to your local machine:

   git clone https://github.com/AaghaFazal/BanALL
   cd BanALL

2. Install Dependencies

   Install the required dependencies:

   pip install -r requirements.txt

3. Set Up Configuration

   Open the config.py file and replace the placeholders for `your_api_id`, `your_api_hash`, and `your_bot_token` with the appropriate values:

   - api_id and api_hash: Create a new application at Telegram Developer Portal (https://my.telegram.org/auth).
   - bot_token: Obtain this from BotFather (https://core.telegram.org/bots#botfather).

   Ensure that remove.txt exists in the same directory. This file will store the log of removed users.

---

Code Improvements:

1. Logging Setup:
   Instead of simply printing errors, the bot will log everything to a log file and the console.

2. Proper Error Handling:
   In case of failures like network issues or permission errors, the bot will log them clearly.

3. Optimized Member Banning:
   Instead of banning members on every message, the bot could perform this action periodically or when a new member joins, reducing unnecessary checks.

4. More Informative Logs:
   The bot will include timestamps and detailed error messages in the log.

5. Graceful Shutdown:
   The bot will handle shutdown gracefully by saving all logs and clearing up resources.

---

Example `config.py`:

```python


api_id = 'your_api_id'         
api_hash = 'your_api_hash'     
bot_token = 'your_bot_token'   

remove_log_file = 'remove.txt'  
