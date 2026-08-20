# Instalação rápida

SERPRO RADAR: Veículo é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_serpro_radar_veiculo`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `SERPRO RADAR: Veículo` / `https://api.mcp.ai/p_serpro_radar_veiculo`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "serpro_radar_veiculo": { "type": "http", "url": "https://api.mcp.ai/p_serpro_radar_veiculo" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=serpro_radar_veiculo&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9zZXJwcm9fcmFkYXJfdmVpY3VsbyJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "serpro_radar_veiculo": { "url": "https://api.mcp.ai/p_serpro_radar_veiculo" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=serpro_radar_veiculo&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_serpro_radar_veiculo%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "serpro_radar_veiculo": { "type": "http", "url": "https://api.mcp.ai/p_serpro_radar_veiculo" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_serpro_radar_veiculo
```

Dúvidas? [serpro_radar_veiculo@mcp.ai](mailto:serpro_radar_veiculo@mcp.ai)
