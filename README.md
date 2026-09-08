# Celonis for Cursor

Connect Cursor to Celonis through MCP.

## Requirements

- A supported Cursor version
- Access to a Celonis team where the MCP endpoint is enabled
- Permission to use the relevant Celonis capabilities

## Install from the Cursor Marketplace

Marketplace installation is the recommended method on Windows, macOS, and
Linux.

1. Open the Plugins or Marketplace page in Cursor.
2. Search for **Celonis**.
3. Select the Celonis plugin and click **Install**.
4. Open the plugin configuration.
5. Continue with [Configure](#configure).

## Configure

1. Install the Celonis plugin from the Marketplace.
2. Open the Celonis plugin configuration.
3. Enter your complete Celonis MCP URL:
   `https://<team>.<realm>.celonis.cloud/mcp`
4. Open Cursor Settings and select Tools & MCP.
5. Connect the `celonis` server.
6. Sign in to Celonis and approve the requested permissions.

No client secret or API key is required.

## Permissions and data flow

Cursor sends MCP requests to the Celonis tenant URL configured by the user.
Celonis authenticates the user and applies tenant, product, package, and
tool-level permissions. Installing the plugin does not grant additional
Celonis permissions.

## Troubleshooting

- OAuth does not start: verify the URL ends in `/mcp` and the endpoint is
  enabled for the tenant.
- Invalid client: verify that `cursor_mcp` is enabled in the tenant's realm.
- Invalid scope: reconnect after confirming the OAuth client allows every
  scope requested by the production MCP endpoint.
- Connected but tools are missing: verify Celonis entitlements and user
  permissions.
- HTTP 403 before OAuth: the production route, policy, or CSRF configuration
  is not allowing OAuth bootstrap traffic.
- Reconnect requested: consent expiry may require renewed authorization.

## Support

Contact: r.devletov@celonis.com
