# Telegram Storage Bot

A simple, self-hosted Telegram Cloud Storage Bot that allows users to upload any file, receive a unique File ID and retrieve it anytime using a deep link. The bot supports all Telegram media types and includes an admin broadcast system.

---

## Features

* 🔐 Private Cloud Storage using Telegram
* 📁 Supports documents, photos, videos, audio, voice, video notes, and text files.
* 🆔 Generates unique File IDs and deep links for easy retrieval.
* 📊 Session-based file statistics.
* 📣 Admin-only announcement/broadcast system.
* 📄 User tracking for announcements (`users.txt`).
* 🧩 Built using Python + python-telegram-bot + pyTelegramBotAPI.

---

## Demo

You can test the bot live:
👉 [@reportcloudstorage\_bot](https://t.me/reportcloudstorage_bot)

---

## Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/itisuniqueofficial/telegram-storage-bot.git
cd telegram-storage-bot
```

### 2️⃣ Install Requirements

```bash
pip install python-telegram-bot==13.15
pip install pyTelegramBotAPI
```

> ⚠️ You must use `python-telegram-bot` version 13.x as your code is written for v13 API.

### 3️⃣ Update Configuration

Edit `bot.py` and replace:

```python
BOT_TOKEN = 'TELEGRAM_BOT_TOKEN'
GROUP_CHAT_ID = TELEGRAM_GROUP_CHAT_ID
ADMIN_ID = TELEGRAM_USER_ID
```

With:

* `BOT_TOKEN`: Your bot token from @BotFather.
* `GROUP_CHAT_ID`: The Telegram Group ID where files will be forwarded and stored.
* `ADMIN_ID`: Your own Telegram User ID for admin-only features.

### 4️⃣ Run the Bot

```bash
python bot.py
```

The bot will start polling and be ready to use.

---

## Usage

### Upload File

* Send any file to the bot.
* The bot will save it, generate a unique File ID and reply with a deep link.

### Retrieve File

* Use the deep link:

```
https://t.me/<your_bot_username>?start=<FileID>
```

### Commands

* `/start` — Start interaction or retrieve file by deep link.
* `/help` — Show usage instructions.
* `/stats` — Show session stats.
* `/announce` — Admin-only: broadcast message (reply to a message).

---

## Announcement System

* Admin can reply to any message with `/announce`.
* The bot will send that message to all users listed in `users.txt`.
* Supports text, photo, video, audio, documents, voice, and video notes.

---

## File Storage Logic

* Files are forwarded and stored inside your specified Telegram group.
* The File ID is simply a combination of timestamp, user ID, and message ID.

---

## File Structure

```
users.txt — All unique user IDs are stored here.
bot.py — Main bot script.
```

---

## Security Notice

* The bot doesn’t store actual files locally.
* Telegram handles the physical file storage inside your group.
* File ID only maps to Telegram group forwarded message IDs.

---

## Credits

* Developed by **It Is Unique Official**
* GitHub: [itisuniqueofficial](https://github.com/itisuniqueofficial)

---

## License

This project is licensed under the MIT License.

---

---

If you want, I can also generate:

* `requirements.txt`
* `LICENSE`
* proper **GitHub description**
* advanced **improved README** with shields, badges, and deployment instructions

Shall I prepare the **full professional GitHub package** for you?
👉 *(You just need to say: "Yes, generate full package")*
