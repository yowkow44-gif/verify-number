How to Use "Verify Number" Telegram Mini App
---------------------------------------------

1. Host this file (index.html) on any HTTPS server:
   - You can use GitHub Pages, Netlify, or Vercel (free).

2. Copy the live link (for example):
   https://yourusername.github.io/verify-number/

3. In your Telegram bot (via Python or Manybot), send a message
   that includes a WebApp button like this:

   Example (Python):
   from telegram import InlineKeyboardButton, InlineKeyboardMarkup

   keyboard = [
       [InlineKeyboardButton("🧾 Open Verify Number App", web_app={"url": "https://yourusername.github.io/verify-number/"})]
   ]
   reply_markup = InlineKeyboardMarkup(keyboard)

   bot.send_message(chat_id=CHAT_ID, text="Click below to open Verify Number app:", reply_markup=reply_markup)

4. When you click "Yes" or "No" inside the app, it sends that result ("yes"/"no") back to your bot.

5. You can view that data in your bot backend or log and manually reply to the customer.
