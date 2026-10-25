# jubilant-sniffle

Project configuration for using the [LinkedIn MCP server](https://pypi.org/project/mcp-server-linkedin/) with Claude Code.

## Setup

1. Install [`uv`](https://docs.astral.sh/uv/), which provides `uvx`.
2. Open Claude Code in this repository. The server is registered in [`.mcp.json`](.mcp.json) as `mcp-server-linkedin`.
3. Approve the server when Claude Code prompts for it.
4. The server may ask you to log in to LinkedIn on first use.

The first start can be slow while `uvx` downloads the package. `UV_HTTP_TIMEOUT` is set to 300 seconds to allow for this.

## Available tools

Once connected, the server exposes tools for:

- Profiles: your own, people, and companies
- Search: people, companies, jobs, and posts
- Jobs: job details, saved jobs, and apply URLs
- Messaging: inbox, conversations, and sending messages
- Feed and company posts, and connection requests

## Notes

- `.mcp.json` uses `mcp-server-linkedin@latest`, so each start picks up the newest release. Pin an exact version for repeatable behaviour.
- Some tools act on your LinkedIn account (sending messages, connection requests). Review these calls before approving them.
