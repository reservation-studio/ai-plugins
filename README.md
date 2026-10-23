# Reservation.Studio plugins

Plugins that connect AI assistants to [Reservation.Studio](https://reservation.business/en).

| Plugin | What it does |
| - | - |
| [`business`](business/) | Ask about the Reservation.Studio business you work in — schedule, availability, clients, services, staff, reports and team tasks — and, when the owner allows it, book, move or cancel appointments. |

## Install

- **Claude**: find **Reservation.Studio Business** in the directory, or in Claude Code run
  `/plugin install reservation-studio-business@reservation-studio` after
  `/plugin marketplace add reservation-studio/ai-plugins`.
- **ChatGPT**: find **Reservation.Studio Business** in Plugins.

Each folder holds the Claude plugin (`.claude-plugin/plugin.json`, `.mcp.json`, `skills/`) and the
[Agent Plugins](https://agent-plugins.org) package used for ChatGPT (`plugin.json`, `mcp.json`) side
by side. The folders are published from Reservation.Studio's own repository; changes made here are
overwritten.

## Support

[help.reservation.studio](https://help.reservation.studio)
