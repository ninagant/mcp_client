# MCP Client

This project provides Python clients for interacting with an MCP (Model Context Protocol) server using different transports (SSE and stdio) and integrates with Anthropic's Claude LLM API.

## Directory Structure
- `claude_llm.py`: Example script to interact with Anthropic Claude LLM using API key from environment variables.
- `llm_sse_client.py`: Client that connects to an MCP server via SSE, sends queries to Claude, and calls tools based on LLM responses.
- `sse_client.py`: Basic SSE client for MCP server, demonstrates tool calls like `get_all_coins` and `get_coin_price`.
- `stdio_client.py`: Client that connects to an MCP server via stdio, demonstrates tool calls similar to `sse_client.py`.
- `requirements.txt`: Python dependencies for the project.

## Requirements
- Python 3.8+
- MCP server (for testing SSE and stdio clients)
- Anthropic API key

## Installation & Setup

1. **Clone the repository**
   ```sh
   git clone <repo-url>
   cd mcp_client
   ```

2. **Create a virtual environment**
   ```sh
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies**
   ```sh
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   - Create a `.env` file in the project root:
     ```env
     ANTHROPIC_API_KEY=your_claude_api_key_here
     ```

5. **Run the clients**
   - Example (Claude LLM):
     ```sh
     python claude_llm.py
     ```
   - Example (SSE Client):
     ```sh
     python llm_sse_client.py
     ```
   - Example (Basic SSE Client):
     ```sh
     python sse_client.py
     ```
   - Example (Stdio Client):
     ```sh
     python stdio_client.py
     ```

## Notes
- Ensure the MCP server is running and accessible at the expected URL/port before running SSE or stdio clients.
- The project uses `python-dotenv` to load environment variables from `.env`.
- The Anthropic Claude API key is required for LLM interactions.
