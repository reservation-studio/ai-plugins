# Reservation.Studio Business

Ask Claude about the Reservation.Studio business you work in, in plain language: who is booked tomorrow, when a stylist is free on Friday afternoon, what last month's revenue was, when a client last came in and what they had done.

## What it includes

- **Connector**: the Reservation.Studio Business MCP server at `https://mcp.reservation.studio/business`. You sign in with your Reservation.Studio account, and Claude sees only what your role allows.
- **Skill `business-questions`**: tells Claude which tools to use, and in which order, for everyday questions about the schedule, availability, clients, reports and tasks.

## Before you start

- You need a Reservation.Studio account with access to a business.
- The owner turns AI connectors on under **Integrations → AI connectors**, and decides who on the team may use them and who may make changes.
- Reports need Reports PRO, and memberships need the memberships feature.

## Use it

Install the plugin, connect **Reservation.Studio Business** from the plugin's Connectors tab, and sign in. Then ask, for example:

- "What appointments do we have tomorrow?"
- "What times are free for a haircut on Friday afternoon?"
- "How much revenue did we make last month?"
- "Book Elena Petrova for a haircut tomorrow at 10:00."

If the owner allows it for you, Claude can also book, move and cancel appointments, block off and unblock time, edit clients and manage tasks. It describes each change first and makes it only after you confirm.

## Data

The plugin sends what your questions need (dates, the names you search for, the records you work with) to Reservation.Studio through `mcp.reservation.studio` and `auth.reservation.studio`, and receives the business data your role can see. The plugin itself stores nothing and sends nothing anywhere else. See the [privacy policy](https://reservation.business/en/privacy-policy).

You can disconnect at any time in Claude, and the owner can switch AI connectors off for the whole business.

## Support

[help.reservation.studio](https://help.reservation.studio)

## License

MIT
