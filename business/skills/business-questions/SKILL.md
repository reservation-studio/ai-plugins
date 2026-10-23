---
name: business-questions
description: Answer questions about a Reservation.Studio business and make changes in it. Use when the user asks about appointments, the schedule, free times, clients and their visits, services, staff, working hours, blocked time, memberships, revenue or other reports, or the team's tasks, or asks to book, move or cancel an appointment.
---

Use the Reservation.Studio Business connector's tools.

1. Call `get-business-context` first. It names the business, its locations, its timezone and its currency. If the user works in several businesses, ask which one.
2. Read dates and times in the business's timezone. "Tomorrow" and "last month" are the business's tomorrow and last month, not the user's.
3. Pick the tool for the question:
   - The schedule for a day or a range: `get-schedule`.
   - Free times for a service: find the service with `list-services`, then `find-available-slots` for one location. If the service has several variants or prices, ask which. Never book while answering this.
   - A client: `find-client`, then `get-client-history` for their profile. For their last visit and what they had done, call `get-schedule` with `client_id`, `date_to` today and `date_from` a month or two back, and take the latest appointment that has started and where they are `attending`; go further back only if none qualifies. If the answer says `truncated`, the newest appointments are the ones cut: move `date_from` closer to today. Don't read `last_visit` as that visit: it can be a cancelled or an upcoming booking.
   - Revenue and other figures: `get-report`. Say which dates the figures cover and in which currency.
   - Staff, working hours, blocked time, memberships and tasks: `list-staff`, `get-working-hours`, `find-blocked-time`, `get-membership-status`, `find-tasks`.
4. To change something, such as booking with `book-appointments`, call the tool once without `confirm`. Show the user the change it describes, in their words, and call again with the returned `confirm` token only after a clear yes.
5. If a tool refuses, tell the user what it says and carry on with what you can read. Retrying won't help.

Answer in the user's language. Summarize instead of pasting lists, and don't show ids.
