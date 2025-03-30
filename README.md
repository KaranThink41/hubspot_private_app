# HubSpot MCP Server
[![smithery badge](https://smithery.ai/badge/@KaranThink41/hubspot_private_app)](https://smithery.ai/server/@KaranThink41/hubspot_private_app)

A Model Context Protocol (MCP) server that provides tools for interacting with HubSpot CRM. This server allows you to create, update, delete, and fetch summary records (stored as Note 
engagements) in HubSpot.

## DockerFile
- docker build -t mcp-hubspot-ts .
- docker run --env-file .env -it mcp-hubspot-ts

## Features

- Create a summary as a Note engagement in HubSpot
- Fetch all summary records (Notes) from HubSpot
- Filter summary records by date
- Update existing summary records
- Delete summary records
- Send summary records via chat or email

## Testing with MCP Inspector

To inspect and test your MCP server implementation, you can use the MCP Inspector. For example:

```bash
npx @modelcontextprotocol/inspector -e HUBSPOT_ACCESS_TOKEN=your_access_token_here node build/index.js
```

This will start the MCP Inspector UI on http://localhost:5173. Use the UI to send JSON-RPC requests to your server.

## Env

Create a `.env` file in the project root with your HubSpot credentials:

```env
HUBSPOT_ACCESS_TOKEN=your_access_token_here
SHARED_CONTACT_ID=your_contact_id_here
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
