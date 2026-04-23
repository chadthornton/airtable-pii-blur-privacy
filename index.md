# Airtable PII Blur — Privacy Policy

_Last updated: 2026-04-23_

Airtable PII Blur ("the extension") is a Chrome browser extension that visually blurs user-configured columns in Airtable grid views. This policy describes what the extension does and does not do with your data.

## What the extension stores

The extension stores the following in Chrome's built-in `chrome.storage.sync` area:

- A master on/off boolean.
- A numeric blur intensity (4–16 px).
- A dictionary mapping Airtable field IDs (e.g. `fldXXXXXXXXXXXXXX`) to a boolean indicating whether that field should be blurred.
- Cached display metadata for the fields you've configured: the field name, the name of the table it belongs to, and a timestamp of when the extension last saw it. This metadata is used solely to render a readable list in the extension's popup.

`chrome.storage.sync` is managed by Chrome and, if you are signed into a Chrome profile with sync enabled, replicated across your devices by Google under Google's own privacy terms. The extension author does not operate any server and does not receive any of this data.

## What the extension does not do

- It does not transmit any data to any remote server.
- It does not read, copy, or extract the contents of cells in your Airtable base.
- It does not use analytics, telemetry, or error reporting.
- It does not load or execute any code fetched at runtime.
- It does not share or sell data to third parties.

## Permissions

- `storage` — to save your preferences as described above.
- `activeTab` — to read the URL of the active tab when the popup is opened, so the popup can scope its display to the Airtable base you currently have open. The extension does not read page content from other tabs.
- Access to `https://airtable.com/*` — required so the content script can observe the Airtable DOM and apply blur styles. The extension runs on no other site.

## Limitations

The extension applies a CSS blur filter. The underlying data remains in the page and in memory and can be revealed by anyone with browser developer tools. This extension is not a security or compliance tool. It is visual cover for screen-sharing only.

## Contact

For questions, issues, or takedown requests: chad.thornton@gmail.com, or open an issue at https://github.com/chadthornton/airtable-pii-blur/issues.
