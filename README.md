# cc-bridge-web

A static web chat UI for [cc-phone-bridge](https://github.com/kaojia/cc-bridge-channel): send commands from your phone to Claude Code running on the laptop, and read the replies as a chat.

🔗 **Live:** https://kaojia.github.io/cc-bridge-web/

## How it works

- Single `index.html`, hosted on GitHub Pages.
- Messages are appended to `inbox.md` in the private repo `kaojia/cc-bridge-channel` via the GitHub Contents API; the laptop bridge picks them up, runs `claude -p`, and writes status and replies to `channel/messages.json`, which this page displays.
- Uses a fine-grained GitHub token that is stored only in your browser's localStorage — it is never committed or sent anywhere except GitHub's API.
