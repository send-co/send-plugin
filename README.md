# Send plugin

Save what you're working on and pick it up in any AI. Publish it as a live
page when you need a link.

Send keeps your notes in your Send workspace, outside any one chat. Save
context in Claude and pick it up in ChatGPT, Cursor or another session, or hand
it to a teammate. When the work needs an audience, Send turns it into a hosted
page at a real URL and tells you who opened it, when, and for how long.

This plugin bundles the hosted Send MCP server and two skills that teach the
agent when to reach for it.

## Install

**Grok Build**

```
grok plugin install send
```

**Claude (Cowork and Claude Code)**

```
/plugin marketplace add send-co/send-plugin
/plugin install send@send
```

**Cursor**

Install from the Cursor marketplace, or add this repo as a source.

Or point any MCP-capable client at the server directly:

```
https://www.send.co/mcp
```

## Authentication

Send uses OAuth 2.1 with dynamic client registration. There is no API key to
copy and nothing to configure.

- Endpoint: `https://www.send.co/mcp` (Streamable HTTP)
- On first tool call your client opens a browser to sign in
- Tokens are held by your client, never by this repository

A free Send account is enough to start. Create one at
[send.co](https://www.send.co).

## What is included

| Component | |
|---|---|
| MCP server | `.mcp.json` — the hosted Send server |
| Skill | `saving-notes-with-send` — save context, pick it up in any AI |
| Skill | `creating-sites-with-send` — when to publish, and the edit loop |

## What it does

- **Save** notes and context to your workspace so they outlive the chat
- **Pick up** saved work in any AI app connected to Send, or share it with your team
- **Create** a hosted page from HTML the agent writes
- **Edit** an existing page so the link you already shared stays good
- **Read back** what is currently published before changing it
- **Manage** sites, link settings and uploaded images

## What people build with it

Landing pages, dashboards, proposals, one-pagers, reports, portfolios and
decks — anything with a reader on the other end. A dashboard is a page like any
other: publish it and the reader gets a live URL instead of a screenshot.

## What it will not do

Send publishes to a public URL. The plugin will not publish without you asking
for it, and the skill instructs the agent to confirm before putting anything
outward-facing at a live link.

## Links

- [send.co](https://www.send.co)
- [Privacy policy](https://www.send.co/legal/privacy-policy)
- [Terms of service](https://www.send.co/legal/terms)
- Support: [support@send.co](mailto:support@send.co) or [open an issue](https://github.com/send-co/send-plugin/issues)
- Privacy questions: [privacy@send.co](mailto:privacy@send.co)
- Security reports: email [support@send.co](mailto:support@send.co), not a public issue

## License

MIT — see [LICENSE](LICENSE).
