# AISDLC_public

Public assets for the Comarch **AI SDLC** programme.

This repository exists so that assets can be fetched over plain HTTPS from anywhere,
without a token. Nothing here is secret, and nothing here is code.

## images/personas/

The five personas the Forge signs its Jira comments with. Each is a 48x48 PNG with
an alpha channel.

| File | Used by |
| --- | --- |
| `triage.png` | the triage flow |
| `analyst.png` | the analyst flow |
| `dev.png` | the development flow |
| `qa.png` | the QA flow |
| `default.png` | Prism, the welcome comment and any flow that cannot be told |

They are served to Jira as raw files, for example:

```
https://raw.githubusercontent.com/dev-green-comarch/AISDLC_public/main/images/personas/dev.png
```

The Forge used to inline these as base64 `data:` URIs, which cost 4,800 to 7,300
characters of every interaction card against Jira's 32,767-character comment limit.
Referencing them by URL gives that room back to the agent's message.
