# RE8CH Qwen Tenant Marketplace

Remote Codex Marketplace for the Qwen tenant. Add this repository once, then
install or refresh its runtime, edge, and expert packages independently.

```sh
codex plugin marketplace add https://github.com/re8ch/qwen-tenant-marketplace.git
```

Packages:

- `re8ch-tenant-runtime@re8ch-qwen-tenant`
- `re8ch-tenant-edge@re8ch-qwen-tenant`
- `re8ch-tenant-expert@re8ch-qwen-tenant`

All packages connect to `https://tools.re8ch.com/tenant/mcp` with OAuth client
`re8ch-qwen-tenant`. Authentication fixes the caller to the Qwen tenant. The
repository contains no user email, access token, kubeconfig, or provider
credential.

The Marketplace can be installed before the backend is enabled, but tools will
remain unavailable until the tenant MCP endpoint and OAuth mapping are live.

WorkBuddy uses the same Streamable HTTP endpoint as a custom MCP connector.
See [`workbuddy/README.md`](workbuddy/README.md).
