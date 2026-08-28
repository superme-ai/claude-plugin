# SuperMe for Claude

Bring trusted perspectives from your SuperMe network into Claude.

This plugin connects Claude to SuperMe's hosted MCP server and includes a workflow for gathering and synthesizing perspectives from the people and experts in your network.

## What it provides

- The live SuperMe MCP toolset through `https://mcp.superme.ai`
- SuperMe authentication through the connector's OAuth flow
- An `ask-your-network` skill that helps Claude find relevant perspectives and synthesize them clearly

The MCP server remains the source of truth for tools and data. Tool updates are available without updating this plugin; the plugin is updated when its workflow guidance or metadata changes.

## Requirements

- A SuperMe account
- Claude Code or another Claude product that supports plugins

## Try it locally

Clone this repository and load it in Claude Code:

```sh
git clone https://github.com/superme-ai/claude-plugin.git
claude --plugin-dir ./claude-plugin
```

Claude will prompt you to connect and authorize SuperMe when a SuperMe tool is first needed.

## Development

Validate the plugin before publishing changes:

```sh
claude plugin validate .
```

When changing the plugin, update the semantic version in `.claude-plugin/plugin.json`.

## Links

- [SuperMe](https://www.superme.ai)
- [Privacy policy](https://www.superme.ai/privacy)
- [Terms](https://www.superme.ai/terms)
- [Support](https://www.superme.ai/support)

## License

[MIT](LICENSE)
