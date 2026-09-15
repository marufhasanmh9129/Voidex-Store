# MYTRIX — Setup Guide

This guide explains how to install and run MYTRIX locally.

## Requirements

- Node.js 18 or newer
- npm
- A Discord application with a bot
- Git (optional)

Check your installed versions:

```bash
node --version
npm --version
```

## 1. Clone the Repository

Clone the repository and enter its directory:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd YOUR_REPOSITORY_NAME
```

## 2. Install Dependencies

```bash
npm install
```

## 3. Configure Environment Variables

Create a `.env` file in the project root. Use the variable names required by the source configuration.

A typical Discord configuration may look like this:

```env
TOKEN=YOUR_DISCORD_BOT_TOKEN
CLIENT_ID=YOUR_CLIENT_ID
GUILD_ID=YOUR_GUILD_ID
```

Do not use real credentials in documentation or commit `.env` to GitHub.

## 4. Configure `.gitignore`

Make sure sensitive and generated files are ignored. At minimum:

```gitignore
node_modules/
.env
.env.*
*.log
```

## 5. Deploy Commands

If your setup requires separate slash-command deployment, run the project's deployment script:

```bash
npm run deploy
```

Make sure the Discord application ID, guild ID, scopes, and permissions are configured correctly.

## 6. Start MYTRIX

For normal use:

```bash
npm start
```

The package configuration starts the bot from `src/index.js`.

## Troubleshooting

### Bot does not start

- Confirm the Node.js version is supported.
- Run `npm install` again.
- Check that `.env` exists and contains the required variables.
- Check the first error shown in the console.

### Commands do not appear

- Confirm the bot is invited to the server.
- Check the required Discord scopes and permissions.
- Run the command deployment step when required.
- Verify `CLIENT_ID` and `GUILD_ID`.

### Token was exposed

Regenerate the Discord bot token immediately and update the local `.env` file. Never commit the old or new token.

## Security

Treat bot tokens, API keys, database credentials, private keys, and session credentials as secrets.

© 2026 MYTRIX
