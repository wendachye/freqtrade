# Local settings

The tracked config contains trading parameters and disabled, empty authentication settings. Compose loads `user_data/config.json` first and ignored `user_data/config.local.json` second.

For a fresh checkout, copy `user_data/config.local.example.json` to `user_data/config.local.json`. Keep Telegram disabled until a replacement token is configured. Generate unique random API passwords, JWT signing secrets and WebSocket tokens locally before enabling the API. Do not reuse credentials from old commits or print replacement credentials in shared terminals.

Never commit local settings. `git check-ignore user_data/config.local.json` must succeed. The example intentionally contains no working credentials. Host API ports remain bound to localhost.

When moving from an older clone whose history contains credentials, use a fresh clone. Do not merge or push the old history back into the cleaned repository.
