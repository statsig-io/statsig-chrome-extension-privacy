---
title: "Statsig Internal Chrome extension: privacy policy"
---

# Statsig Internal Chrome extension: privacy policy

Last updated: 2026-11-12

Statsig Internal is a Chrome extension for Statsig and Amplitude employees, distributed privately to the Amplitude Google Workspace. This policy describes what it handles.

## Where data goes

The extension talks to one server: www.statsig.me, Statsig's internal tools site, using your existing statsig.me sign-in. It also downloads reward images from raw.githubusercontent.com, which receives no user data.

## What the extension handles, and why

| Data | Used for | Where it goes |
|---|---|---|
| Your statsig.me session cookie | Authenticating requests to www.statsig.me | Sent only to www.statsig.me by Chrome. The extension never reads, stores or forwards it |
| Your statsig.me email address | Fetching your own reward feed; shown in the popup | Read from www.statsig.me and sent back only to www.statsig.me to fetch your feed. Cached for up to 10 minutes in session storage |
| Statsig IDs or client SDK keys you look up with Lens | Showing what the ID refers to | Only a validated ID or client key is sent to www.statsig.me. Secret and console keys are refused and never sent or stored |
| Commands and company names you type in the Statsig bar | Running internal shortcuts and company search | Sent to www.statsig.me when you press Enter, or (company search) after 3 characters |
| Pull request numbers in statsig-io/statsig | Deploy status for Landed? | Sent to www.statsig.me when you click the chip or turn on auto-check |
| Merge clicks on GitHub, status changes on Linear | Prompting an immediate check of your reward feed | Not sent anywhere; they only start a check of your own feed |
| Statsig SDK state on pages you inspect | Showing evaluations and events in SDK Inspector | Stays in the tab. Never stored or sent |
| The address of your current tab, when you use the Customer card | Working out which customer the page is about | Read and parsed in your browser. Only one token is sent to www.statsig.me per lookup: an Unthread conversation ID, a Statsig project ID taken from a console or intern address, or an email domain you type (the email is reduced to its domain in your browser). The page address, title and text are never sent. Personal email domains, Statsig and Amplitude domains, and secret or console keys are refused locally |
| Customer card results | Showing the customer card | Cached in session storage for 5 to 60 minutes. Your last 10 customers (ID and name) and a list of the requests the card made in the last 24 hours are also kept in session storage. Session storage is cleared when Chrome closes |
| Settings, recent lookups, opted-in sites, overrides, deploy watches | Remembering your choices | Your browser's local extension storage only. Overrides are deleted after 60 minutes, watches after 48 hours |
| Feature on/off list from www.statsig.me | Letting Statsig turn a feature off without a release | Read about every 30 minutes with your sign-in; nothing else is sent. The answer (feature names and a message) is kept in local storage |

## Limited Use

The use of information received from Google APIs and from your browser by this extension adheres to the Chrome Web Store User Data Policy, including the Limited Use requirements.

## What it does not do

- No analytics, telemetry, advertising or tracking.
- No data is sold, shared with third parties, or used for anything other than the features above.
- No remote code. All code ships in the extension package.

## Your controls

- Remove the extension in chrome://extensions to delete everything it stored.
- Clear recent lookups and recent customers with the Clear buttons.
- Remove sites from SDK Inspector in its Sites tab.

## Contact

Questions or requests: open an issue at https://github.com/statsig-io/statsig-chrome-extension-privacy/issues.
