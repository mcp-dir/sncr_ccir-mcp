# Instalação detalhada

SNCR: Emissão do Certificado de Cadastro do Imóvel Rural (CCIR) é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_sncr_ccir`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_sncr_ccir` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_sncr_ccir` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_sncr_ccir` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.sncr_ccir` (ou `servers.sncr_ccir` no VS Code) do config do cliente e reinicie.
