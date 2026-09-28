# Petro Host Bot — Free Hosting Ready

This package is prepared from the supplied `petro host bot (1).py`.

## Files
- `bot.py` — bot source
- `requirements.txt` — Python dependencies
- `.env.example` — environment-variable template
- `Procfile` — worker start command
- `start.sh` — simple start script
- `render.yaml` — deployment template

## Required environment variables
- `TOKEN` — Telegram BotFather token
- `OWNER_ID` — Telegram numeric user ID

Optional: `ADMIN_ID`, `YOUR_USERNAME`, `UPDATE_CHANNEL`, `FREE_USER_LIMIT`, `SUBSCRIBED_USER_LIMIT`, `ADMIN_LIMIT`.

## Start command
`python bot.py`

## Important
The bot stores SQLite data and uploaded files locally (`inf/bot_data.db` and `upload_bots/`). A free host with ephemeral storage may lose those files after a restart/redeploy. Use persistent storage or an external database/storage service if the data must survive restarts.

The included Flask keep-alive endpoint does not guarantee that a hosting provider will keep a free service running 24/7. The host's own sleep/usage policy still applies.
