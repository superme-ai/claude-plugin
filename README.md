# SuperMe MCP for Claude

Find and ask experts.

This plugin packages the existing SuperMe remote MCP connector for Claude's plugin directory. It points to the same hosted server as the SuperMe connector and does not add a separate tool or workflow layer.

## What it provides

- Resolve and read profiles in your professional network
- Discover experts on a topic
- Ask a person, community, or workgroup a question
- Use your SuperMe agent and manage workgroups
- Authenticate through SuperMe's existing OAuth connector flow

The live MCP server at `https://mcp.superme.ai` remains the source of truth for tools, authentication, and data. Server tool updates are available without updating this plugin.

## Example prompts

- Find me the best experts on product-led growth.
- Ask Elena Verna, Kyle Poyar, and Ben Williams about the biggest mistakes companies make with PLG.
- Ask Mercedes Bent how she evaluates investments?

## Requirements

- A SuperMe account
- Claude Code or another Claude product that supports plugins

## Connect SuperMe

The plugin already includes the SuperMe MCP connection, so you do not need to add the server manually.

1. Install and enable the plugin.
2. Ask Claude to connect to SuperMe, or make a request that needs a SuperMe tool.
3. Open the authorization URL that Claude displays.
4. Log in to your SuperMe account and approve the connection.
5. If Claude asks after login, paste the full browser redirect URL back into the conversation to complete authentication.

If no authorization URL appears in Claude Code, run `/mcp`, select SuperMe, and choose **Authenticate**.

## Try it locally

Clone this repository and load it in Claude Code:

```sh
git clone https://github.com/superme-ai/claude-plugin.git
claude --plugin-dir ./claude-plugin
```

For direct MCP installation without this plugin, use the generated command under [SuperMe Settings → MCP Access](https://www.superme.ai/settings?tab=agent-setup). Do not install both methods unless you intentionally want a separate direct MCP configuration.

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
