# Installing the Quantum Metric MCP server in Cline

The server URL is `https://api.quantummetric.com/mcp`. It uses OAuth, so no API key or token is needed.

1. Find Cline's MCP settings file, which is named `cline_mcp_settings.json`.
   - Cline CLI: `~/.cline/data/settings/cline_mcp_settings.json` (or the path in the `CLINE_MCP_SETTINGS_PATH` environment variable).
   - Cline in VS Code, Cursor and other editors: the MCP Servers icon, then the Configure tab, then Configure MCP Servers opens the file.
2. If the file does not exist, create it with the contents of `cline_mcp_settings.example.json`. If it exists, add the `quantum-metric` entry from that file to its `mcpServers` object and keep every other server.
3. Keep `"type": "streamableHttp"`. Without it Cline treats the URL as a legacy SSE server.
4. Tell the user to authorize the server and sign in to Quantum Metric when Cline asks (in the CLI, `cline mcp` has an Authorize OAuth action). The user chooses their subscription at sign-in.

You do not need to read any other file under `~/.cline`. Do not open `providers.json`, which contains credentials.
