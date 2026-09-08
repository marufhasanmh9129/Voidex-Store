## Prefix Command System

This build uses one per-server prefix for all loaded commands.

### How it works

- Default prefix: `?`
- Change it with `/setprefix prefix:<prefix>`.
- `/setprefix` is **Administrator only** and remains slash-only.
- After changing the prefix, **all loaded slash commands can also be used with the new server prefix**.
- Slash commands continue to work normally.
- Prefix command permissions match the slash command permissions. Commands that declare `default_member_permissions` keep the same restriction when used with the prefix.
- Command-specific permission checks inside command files are also preserved.

### Examples

If the server prefix is `!`:

- `!serverinfo`
- `!userinfo @User`
- `!ban @User reason`
- `!clear 10`
- `!timeout @User 10m reason`
- `!set vouchchannel #vouches`
- `!autoreact add hello 👋`
- `!giveaway start ...`

Subcommands use the same format as slash commands:

- `!warn add @User reason`
- `!extraowner list`
- `!whitelist list`
- `!set requestchannel #requests`

### Option formats

Prefix options support:

- Normal positional arguments: `!ban @User reason`
- Quoted text: `!say "hello world"`
- Named options: `!ban --user @User --reason "bad behavior"`
- `--option=value`: `!ban --user=@User --reason="bad behavior"`
- User mentions: `@User`
- Role mentions: `@Role`
- Channel mentions: `#channel`
- User/role/channel IDs where applicable

The prefix is stored per server in `src/data/prefixes.json`.
