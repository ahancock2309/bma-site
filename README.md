# businessmentorshipacademy.com

Static site for the Business Mentorship Academy (a trading name of Peak 9 Ltd), plus one Netlify function.

- `index.html`, `thanks.html`, `terms.html`: the pages. Booking switch: the `BOOKING` config near the end of index.html. Chat switch: `var CHAT = { live: ... }`.
- `netlify/functions/chat.mjs`: website chat at `/api/chat`. It answers only from `bma-facts.mjs`, which is generated from the fact sheet kept in the project Library (bma/chatbot/facts.md). Needs `ANTHROPIC_API_KEY` in Netlify env.
- Visitor questions the bot can't answer go to the Netlify form `ask-team`.

Deploys: every push to `main` builds on Netlify (repo is public so the free plan builds it).
