
# Bruno MCP Server

A containerized version of "Bruno MCP Server"

> Repository: [hungthai1401/bruno-mcp](https://github.com/hungthai1401/bruno-mcp)

## Description

An MCP (Model Context Protocol) server that enables running Bruno collections. This server allows LLMs to execute API tests using Bruno and get detailed results through a standardized interface.


## Usage

The containers are built automatically and are available on the GitHub Container Registry.

1. Pull the Docker image:

```bash
docker pull ghcr.io/metorial/mcp-container--hungthai1401--bruno-mcp--bruno-mcp
```

2. Run the container:

```bash
docker run -i --rm \ 
ghcr.io/metorial/mcp-container--hungthai1401--bruno-mcp--bruno-mcp  "node ./build/index.js"
```

- `--rm` removes the container after it exits, so you don't have to clean up manually.
- `-i` allows you to interact with the container in your terminal.




## Usage with Claude

```json
{
  "mcpServers": {
    "bruno-mcp": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "ghcr.io/metorial/mcp-container--hungthai1401--bruno-mcp--bruno-mcp",
        "node ./build/index.js"
      ],
      "env": {}
    }
  }
}
```

# License

Please refer to the license provided in [the project repository](https://github.com/hungthai1401/bruno-mcp) for more information.

## Contributing

Contributions are welcome! If you notice any issues or have suggestions for improvements, please open an issue or submit a pull request.

<div align="center">
  <sub>Containerized with ❤️ by <a href="https://metorial.com">Metorial</a></sub>
</div>
  