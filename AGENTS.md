# Documentation project instructions

## About this project

- Public documentation site for the FreightPOP MCP Server, built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Audience: FreightPOP customers who want to run freight operations through an AI client, plus directory reviewers at Anthropic and OpenAI

## Hard constraints

- **Tool names must match the production server exactly.** Never invent, shorten, or prettify a tool name. The production server is `https://tms-mcp.freightpop.com/mcp`. If you cannot verify a tool name, ask rather than guess.
- **The connector URL is `https://tms-mcp.freightpop.com/mcp`**, including the path. It must be byte-identical everywhere it appears.
- **Never commit placeholder or lorem-ipsum content.** No `placeholder-*.png` references, no "Describe how to install your product" boilerplate. Broken images and template text fail directory review.
- **Never leave a heading with no body.** An empty section reads as an incomplete privacy disclosure.
- Do not make claims about data retention, subprocessors, or model-training policies that are not already stated in the FreightPOP Privacy Policy.

## Terminology

- "AI client" for Claude Desktop, Claude.ai, ChatGPT collectively. Not "LLM", not "assistant".
- "connector" for the thing a user adds in their AI client. Not "integration", not "plugin".
- "shipment" and "order" are distinct objects in FreightPOP. Do not use them interchangeably.
- "read-only" and "write" for tool types. Cancellation is "write (destructive)".
- "FreightPOP web app" for the main product UI.

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise, one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for tool names, file names, commands, and paths
- Every tool page includes at least one realistic example prompt
- Prefer plain words over jargon. Avoid em dashes.

## Content boundaries

- Document only what a customer can do through an AI client. Internal admin features, feature flags, and infrastructure details are out of scope.
- Do not document endpoint paths, DTO class names, or internal API routes. Those are implementation details and read as sloppy to reviewers.
- Do not document tools that exist only on the test server.
