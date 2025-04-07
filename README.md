# Quickstart Resources

A repository of servers and clients from the following Model Context Protocol tutorials:
- [Quickstart](https://modelcontextprotocol.io/quickstart) – a simple MCP weather server
- [Building MCP clients](https://modelcontextprotocol.io/tutorials/building-a-client) – an LLM-powered chatbot MCP client


## Weather client

**Claude Desktop**
_add mcp build folder or copy index.js build to your mcp server folder_ 

```bash
./weather-server-typescript/weather/build/index.js
```
**claude_desktop_config.json**
```JSON
{
    "mcpServers": {
        "weather": {
            "command": "node",
            "args": [
                "C:\\PATH\\TO\\PARENT\\FOLDER\\weather\\build\\index.js"
            ]
        }
    }
}
```

**Cursor**
- _select_ Agent^ in chat box, then click on the "..." on the top right
- _click_  **+Add new global MCP server**
- setup **json** file accordingly (https://docs.cursor.com/context/model-context-protocol):

Or as a minimal example:
```JSON
{
    "mcpServers": {
        "weather": {
            "command": "node",
            "args": [
                "C:\\PATH\\TO\\PARENT\\FOLDER\\weather\\build\\index.js"
            ]
        }
    }
}
```


**Tools**
- get-alerts
- get-forecast

### Build

**_linux_**
```bash
npm run build
```

**_windows_**
```bash
npm run buildwin
```