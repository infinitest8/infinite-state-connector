# Infinite State Meditations

A read-only MCP connector for three selected free Infinite State binaural-beat
sessions. Intended for the Cursor Marketplace and Grok Bot. This package is not
yet approved or listed in the marketplace.

## Setup

No Infinite State account, API key, payment, or OAuth sign-in is required.
The package's `mcp.json` connects to the public Streamable HTTP endpoint:
https://infinite-state-muse.onrender.com/mcp/grok.

For local testing, import this package through Cursor's supported local plugin
flow and enable its MCP server. Marketplace installation will be available only
after acceptance. In Grok Bot, an accepted listing is installed from Plugins;
attach the installed connector to a task with `@`.

## Recommendations

The `recommend_session` tool accepts a brief `user_context` (1-1000 characters).
Optional inputs: `desired_outcome` (STRESS, SLEEP, or FOCUS when explicitly
stated), `desired_duration` (positive minutes, at most 1440), and
`content_preference` (1-200 characters).

It returns a normalized goal, title, description, actual duration, concise
reason, listening URL, free/premium status, heuristic confidence, and a
clarification question when intent is ambiguous. It does not play audio,
modify accounts, diagnose conditions, or process payments.

All clients use the same user-selected sessions:

| Goal | Session | Duration | Access |
| --- | --- | --- | --- |
| STRESS | REDUCE STRESS w/ ALPHA BINAURAL BEATS | 11:11 | Free |
| SLEEP | DRIFT OFF TO DEEP SLEEP w/ DELTA BINAURAL BEATS | 55:55 | Free |
| FOCUS | INCREASE FOCUS w/ BETA BINAURAL BEATS | 22:22 | Free |

Session lengths are fixed, even when a different duration is requested.
Open the returned URL to listen on Infinite State. This is general wellness
content, not medical advice, diagnosis, or treatment.

Example prompts:

- "I am overwhelmed and need to calm down before a meeting."
- "I cannot fall asleep and want to drift off."
- "I need to finish a report and cannot concentrate."

## Privacy Policy

Only a brief immediate goal and relevant next activity are needed. Do not supply
medical records, full conversation histories, memories, or unrelated personal
information. Requests are sent to Infinite State's Render-hosted service and
processed transiently. The application does not persist requests or log request
bodies. Render dashboard service logs have seven-day retention on the current
Hobby workspace; separate provider metadata follows Render's policies.

Listening links include `utm_source=grok`, `utm_medium=connector`, and
`utm_campaign=infinite_state_meditations`. Opening a listening link is a separate
interaction with the Infinite State website.

Privacy policy: https://www.infinitestate.app/privacy-policy.
Service terms: https://www.infinitestate.app/terms-and-conditions-service.
API documentation: https://infinite-state-muse.onrender.com/docs.
Privacy, deletion, and support inquiries: hello@infinitestateapp.com.

## License and Content Rights

The connector configuration and documentation are MIT-licensed; see LICENSE.
The logo in `assets/logo.png` is excluded from that license. It is provided only
to identify the official Infinite State connector, not to imply endorsement of
modified versions. No trademark rights are granted. See NOTICE.md.

The hosted service implementation and meditation audio are not included in this
package and are not licensed by this package's MIT license.
