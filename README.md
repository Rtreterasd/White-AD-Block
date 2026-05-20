# Ad Blocker for YouTube

**Ad Blocker for YouTube** is a minimal Chrome extension for blocking ads on YouTube only.

The extension has one narrow purpose: reduce advertising interruptions on YouTube pages while keeping the interface simple and transparent.

## Features

- Blocks YouTube ad-related requests with Manifest V3 Declarative Net Request rules.
- Hides common YouTube ad containers and overlays locally in the browser.
- Adds one On/Off switch for YouTube ad blocking.
- Shows an ON/OFF badge on the extension icon.
- Provides quick links to support the project and read the Privacy Policy.
- Uses Russian by default and English when the browser UI language is English.

## Single Purpose

The single purpose of this extension is to block ads on YouTube websites:

- `https://www.youtube.com/*`
- `https://m.youtube.com/*`
- `https://www.youtube-nocookie.com/*`

The extension does not block ads on other websites, does not manage tabs, does not block popups outside YouTube, and does not include unrelated browser tools.

## Permissions

The extension requests only the permissions needed for its single purpose.

| Permission | Why it is used |
| --- | --- |
| `storage` | Stores the local On/Off state so the extension remembers the user's choice between browser sessions. |
| `declarativeNetRequest` | Applies browser-level blocking rules for YouTube ad-related network requests without reading request contents. |
| YouTube host permissions | Runs the content scripts only on YouTube domains, where ad elements need to be hidden or skipped. |

## Privacy

The extension runs locally in the browser.

It does not collect, sell, or transmit personal data to a server. The only persistent setting is the local On/Off state. See [PRIVACY.md](PRIVACY.md) for the full Privacy Policy.

## Installation For Testing

1. Open `chrome://extensions/`.
2. Enable **Developer mode**.
3. Click **Load unpacked**.
4. Select this project folder.

## Repository Files

- `manifest.json` - Chrome extension manifest.
- `background.js` - Dynamic blocking rules and badge state.
- `youtube-content.js` - YouTube page controls and cosmetic hiding.
- `youtube-page.js` - YouTube in-page response cleanup.
- `popup.html`, `popup.css`, `popup.js` - Minimal extension interface.
- `PRIVACY.md` - Privacy Policy for GitHub and Chrome Web Store.
- `privacy-policy.html` - Public HTML version of the Privacy Policy.
- `WEBSTORE.md` - Ready-to-use Chrome Web Store listing text.

## Disclaimer

YouTube is a trademark of Google LLC. This extension is not affiliated with, endorsed by, sponsored by, or approved by Google LLC or YouTube.
