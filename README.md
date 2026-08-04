# FreightPOP MCP Documentation

Public documentation for the **FreightPOP MCP Server**, which connects a FreightPOP account to AI clients (Claude Desktop, Claude.ai, ChatGPT) over the Model Context Protocol.

Live site: https://docs.freightpop.com
Connector URL: `https://tms-mcp.freightpop.com/mcp`

## What's here

| Path | Contents |
| --- | --- |
| `index.mdx` | Landing page and overview |
| `getting-started.mdx` | Connect an AI client and run a first prompt |
| `clients/` | Per-client setup guides (Claude Desktop, Claude.ai, ChatGPT, Microsoft Copilot) |
| `tools/` | Reference for each tool the server exposes |
| `authentication.mdx` | OAuth flow, session handling, data handling |
| `troubleshooting.mdx` | Common failures and fixes |
| `support.mdx` | How to reach support |
| `docs.json` | Site config and navigation |

## Keeping the tool reference accurate

The pages under `tools/` must match the tools the production server actually exposes. When a tool is added, removed, or renamed on `tms-mcp.freightpop.com`, update:

1. The relevant page under `tools/`
2. The full tool list table in `tools/overview.mdx`
3. `docs.json` navigation, if a page was added or removed

Directory reviewers (Anthropic, OpenAI) compare these docs against the live tool list, so a mismatch is a submission blocker.

## Privacy policy

Data handling for the MCP Server is documented in [`authentication.mdx`](./authentication.mdx). The authoritative company policy lives at:

- Privacy Policy: https://www.freightpop.com/privacy
- Terms & Conditions: https://www.freightpop.com/terms-conditions

Both must stay publicly reachable over HTTPS. They are a hard requirement for the Claude Connectors Directory and the OpenAI app directory.

## Local development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```
npm i -g mint
```

Run at the repo root, where `docs.json` lives:

```
mint dev
```

Preview at `http://localhost:3000`. Run `mint update` if the CLI misbehaves.

## Publishing

Changes to the default branch deploy automatically via the Mintlify GitHub app.

## Support

support@freightpop.com
