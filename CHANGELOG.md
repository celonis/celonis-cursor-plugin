# Changelog

All notable changes to this plugin will be documented here.

## 1.0.0 — initial release

- Logo: Celonis official mark on a black 400×400 background plate.
- Added the `celonis` MCP server backed by the Celonis tenant MCP endpoint at `${CELONIS_MCP_URL}`.
- Declared `CELONIS_MCP_URL` plugin variable so each team can point at its own `https://<team>.<realm>.celonis.cloud/mcp` URL.
- Configured OAuth with the public `cursor_mcp` client (authorization code + PKCE; no client secret).
- Pinned OAuth scopes to `studio-mcp`, `data-pipelines.data:read`, `data-pipelines:manage`, `knowledge-models:read`, `package-manager`, `pig-semantic-layer:read`, `pql-assistant:generation`, and `mcp-asset.tools:execute`.
