# Homestead Companion in-app announcements

The Android app reads `announcements.json` from this repository through GitHub Pages.

## Publish a message

1. Edit `announcements.json`.
2. Use a **new unique `id`** only when the message should be eligible to auto-open once.
3. Use the same ID to correct or update an inbox message without showing it automatically again to people who already saw it.
4. Commit the change and verify [the live feed](https://pyledesignz.github.io/homestead-companion-legal/announcements.json).

Use `"presentation": "inbox-only"` for routine updates and `"presentation": "popup"` only for messages important enough to appear once when the app opens. If several new popup messages arrive together, the app presents only the highest-priority one; the others remain in the inbox.

Allowed categories are `welcome`, `update`, `maintenance`, `news`, and `support`. Allowed actions are `support`, `privacy`, `terms`, and `play-subscriptions`. The app rejects HTML, arbitrary links/actions, duplicate IDs, unknown fields, malformed dates, and invalid JSON.

See the existing JSON object for the complete field shape. Do not publish secrets, customer data, or urgent safety instructions. Changes may take a few minutes to appear through GitHub Pages.
