# Quantum Metric for Cline

Analyze funnels, errors, friction and session replays in Quantum Metric to find and fix digital experience issues.

## Install

Add the server to Cline's MCP settings file, `cline_mcp_settings.json`.

- **Cline CLI:** `~/.cline/data/settings/cline_mcp_settings.json`. Running `cline mcp` opens a wizard that edits it.
- **Cline in VS Code, Cursor and other editors:** click the MCP Servers icon, open the Configure tab, then choose Configure MCP Servers.

Add the entry from `cline_mcp_settings.example.json` to the `mcpServers` object, keeping `"type": "streamableHttp"`:

```json
{
  "mcpServers": {
    "quantum-metric": {
      "type": "streamableHttp",
      "url": "https://api.quantummetric.com/mcp",
      "disabled": false
    }
  }
}
```

Then authorize the server and sign in to Quantum Metric when Cline asks.

## Configure

The server uses Quantum Metric sign-in (OAuth). Every call runs as you, with your role, permissions, workspace and timezone. No token is created or stored.

| Setting | Value |
|---|---|
| Endpoint | `https://api.quantummetric.com/mcp` |
| Subscription | Chosen when you sign in |

## Support

support@quantummetric.com, or the [Quantum Metric support portal](https://thequad.quantummetric.com/).

## Privacy

[Quantum Metric Privacy Policy](https://www.quantummetric.com/legal/privacy-policy)

## Terms

[Quantum Metric Terms and Conditions](https://iam.quantummetric.com/terms-and-conditions)

## License

MIT
