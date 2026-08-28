# SuperMe MCP for Claude

Access your professional network from Claude.

This plugin packages the existing SuperMe remote MCP connector for Claude's plugin directory. It points to the same hosted server as the SuperMe connector and does not add a separate tool or workflow layer.

## What it provides

- Resolve and read profiles in your professional network
- Discover experts on a topic
- Ask a person, community, or workgroup a question
- Use your SuperMe agent and manage workgroups
- Authenticate through SuperMe's existing OAuth connector flow

The live MCP server at `https://mcp.superme.ai` remains the source of truth for tools, authentication, and data. Server tool updates are available without updating this plugin.

## Requirements

- A SuperMe account
- Claude Code or another Claude product that supports plugins

## Try it locally

Clone this repository and load it in Claude Code:

```sh
git clone https://github.com/superme-ai/claude-plugin.git
claude --plugin-dir ./claude-plugin
```

Claude may prompt you to authorize SuperMe when a SuperMe tool is first needed. If authentication is required in Claude Code, run `/mcp`, select `superme`, and choose **Authenticate**.

## Development

Validate the plugin before publishing changes:

```sh
claude plugin validate --strict .
```

When changing plugin metadata or configuration, update the semantic version in `.claude-plugin/plugin.json`.

## Links

- [SuperMe](https://www.superme.ai)
- [Privacy policy](https://www.superme.ai/privacy)
- [Terms](https://www.superme.ai/terms)
- [Support](https://www.superme.ai/support)

## License

[MIT](LICENSE)
