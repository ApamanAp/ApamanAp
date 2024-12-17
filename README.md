from telegram import Update
from telegram.ext import Updater, CommandHandler, MessageHandler, Filters, CallbackContext

# Start command handler
def start(update: Update, context: CallbackContext) -> None:
    update.message.reply_text('Hello! I am a secure bot. How can I assist you today?')

# Main function to start the bot
def main():
    # Add your bot token here
    updater = Updater("7300771774:AAHIyHZErc6jawxgUC6dPSwz7HZVY4SnWjA")

    # Get dispatcher to register handlers
    dispatcher = updater.dispatcher

    # Register command handlers
    dispatcher.add_handler(CommandHandler("start", start))

    # Start the bot
    updater.start_polling()
    updater.idle()

if __name__ == "__main__":
    main()
