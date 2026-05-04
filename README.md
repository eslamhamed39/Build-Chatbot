# Chatbot Backend Production Build

This folder contains the production-ready chatbot backend build.

## 1. Install Dependencies

```bash
npm install --omit=dev
```

## 2. Configure Environment

Copy the example environment file and update values for your server:

```bash
cp .env.example .env
```

Important values in `.env`:

```env
PORT=8080
DB_FILE=./chatbot.db
CORS_ORIGIN=https://your-frontend-domain.com
SYNC_KEY=your_secret_key_min_32_chars_here_change_me
```

Keep `.env` private and do not commit it to GitHub.

## 3. Run The Build

```bash
npm run start:dist
```

## 4. Check Health

Open this URL:

```bash
http://localhost:8080/health
```

If you change `PORT` in `.env`, use the updated port in the health URL.

## Notes

- `dist/app.cjs` is the built application entry point.
- `chatbot.db` must exist, or `DB_FILE` must point to the correct database path.
- `CORS_ORIGIN` must match the frontend domain that will call the chatbot API.
- Runtime folders such as `logs`, `backups`, and `exports` are intentionally ignored by Git.
