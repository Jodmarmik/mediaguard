# Telegram Media Deleter Bot

Deletes media in groups after a delay (default 5 minutes). Sends confirmation after clearing.

## Features
- Deletes photos, videos, stickers, documents, gifs, audio, voice etc. after the configured delay.
- Per-group toggle with `/mediaon` and `/mediaoff` (group-admin only).
- Owner-only `/broadcast` to broadcast to all known groups.
- `start` message with inline buttons to support group/chat.
- Uses MongoDB to persist group settings.

## Deploy to Heroku
1. Create a Heroku app.
2. Set config vars:
   - `BOT_TOKEN` (from BotFather)
   - `MONGO_URI` (MongoDB URI)
   - `OWNER_ID` (your Telegram numeric id)
   - Optionally `DEFAULT_DELAY`, `SUPPORT_GROUP_URL`, `SUPPORT_CHAT_URL`
3. Push this repo to Heroku (or use the Deploy to Heroku button).
4. Add the bot to your groups and give it **Delete messages** permission.

## Notes
- The bot cannot add you to any group. You must invite the bot to the group.
- If you prefer webhooks, you'll need to adapt the `Procfile` and provide `WEBHOOK_URL`.
