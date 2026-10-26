# GWS Read-Only Automation — legal pages

Public app-home and privacy-policy pages for a private, single-operator Google OAuth client
used by an internal **read-only** Google Workspace automation tool. These pages exist because
Google requires an external OAuth app to publish an application home page and a privacy policy
before it can be moved from *Testing* to *In production*.

- App home: https://victor-mai.github.io/gws-legal/
- Privacy policy: https://victor-mai.github.io/gws-legal/privacy.html

## Contents

| File | Purpose |
|---|---|
| `index.html` | Application home page: what the tool does, which Google scopes it reads, contact |
| `privacy.html` | Privacy policy: data accessed, use, storage, sharing, Limited Use statement, retention/deletion |
| `.github/workflows/pages.yml` | Deploys the two pages to GitHub Pages on every push to `main` |

## Notes

- The tool requests only `.readonly` scopes (Drive, Sheets, Docs, Slides, Forms, Gmail,
  Calendar, Contacts). It has no write, send, delete, or sharing capability.
- No Google user data is stored in this repository.
