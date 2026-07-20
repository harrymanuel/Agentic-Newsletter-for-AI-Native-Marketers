# Marketing Automations

Automations I've built in Make.com. Each folder contains the exported blueprint, which you can import straight into any Make account and inspect module by module.

## AI Newsletter Digest

**Gmail → Claude → Slack**

I subscribe to a lot of marketing and AI newsletters. Most of it is noise. This automation reads them so I don't have to.

Every morning it pulls the last 24 hours of newsletters from a dedicated Gmail inbox, merges them into a single block of text, and sends it to Claude with a prompt I wrote to act as a briefing assistant. The prompt is fairly opinionated: it tells the model exactly what I care about (AI tooling, marketing strategy, SEO, design, no-code building), sets a quality bar so filler and sponsored content get binned, and enforces Slack-friendly formatting rules so the output renders cleanly. If nothing in that day's newsletters is worth knowing, it says so in one line instead of padding out a summary.

The result lands in a private Slack channel as a short daily digest. Reading time went from 30+ minutes of skimming to about 90 seconds.

**Stack:** Make.com, Gmail API, Anthropic Claude (Haiku, because the task doesn't need a bigger model and cheaper runs matter when it fires daily), Slack API.

**To run it yourself:** import `blueprint.json` into Make, connect your own Gmail and Slack accounts, and swap in your own interests in the Claude prompt.
