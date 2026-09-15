# MYTRIX

> All-in-one Discord bot for moderation, utilities, automation, music, server management, and more.

## Features

- 🛡️ Moderation and permission management
- 👋 Welcome and auto-role systems
- 📋 Logging and server configuration
- 🎁 Giveaway and utility commands
- 🎵 Music and Lavalink integration
- 📊 Server statistics and automation

## Requirements

- Node.js 18 or newer
- npm
- A Discord application and bot
- Git (optional)

## Quick Start

1. Clone the repository.
2. Install dependencies.
3. Create and configure your environment file.
4. Start the bot.

See **[SETUP.md](SETUP.md)** for the complete setup guide.

## Environment Variables

Keep secrets in `.env` and never commit them to GitHub. Use `.env.example` when available as a template.

Typical variables may include:

- `TOKEN`
- `CLIENT_ID`
- `GUILD_ID`
- Database or Lavalink settings used by your configuration

The exact variables depend on the source configuration.

## Music Search Sources

If music search is enabled, `MUSIC_SEARCH_SOURCES` can contain a comma-separated list of search prefixes supported by the connected Lavalink node.

Example:

```env
MUSIC_SEARCH_SOURCES=ytsearch,ytmsearch,scsearch,spsearch,dzsearch,amsearch,tdsearch,qbsearch,ymsearch,vksearch,jssearch,pdsearch,bcsearch
```

The prefixes only work when the corresponding source or plugin is available on the Lavalink node. Setting an environment variable does not install or enable a music source by itself.

## Useful Commands

The available commands depend on the enabled modules and current source configuration. Examples include:

- `/help`
- `/ping`
- `/serverinfo`
- `/userinfo`
- `/giveaway`

## Project Structure

```text
src/
├── commands/
├── handlers/
├── config/
├── data/
└── index.js
```

## Security

Never publish or commit:

- Discord bot tokens
- API keys
- Database credentials
- Private keys
- Other authentication secrets

If a token is exposed, revoke or regenerate it immediately.

## License

This project is distributed under the license included in the repository.

## Disclaimer

MYTRIX is not affiliated with, sponsored by, or endorsed by Discord. Discord and its trademarks belong to their respective owners.

© 2026 MYTRIX
