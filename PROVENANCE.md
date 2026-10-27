# Source and validation

This extension reuses the MIT-licensed Postedly task skills, references and icon from [Soxoa's Claude plugin repository](https://github.com/johnarndt/soxoa-claude-plugins/tree/2bc7d09dbae17735ddfd008eeaf75bba1b02e4af/postedly), commit `2bc7d09dbae17735ddfd008eeaf75bba1b02e4af`.

The Gemini CLI distribution adds a root `gemini-extension.json`, Gemini context and installation documentation. Platform-specific connection help is adapted to Gemini CLI. Product actions continue through Postedly's existing hosted MCP server; this repository contains no server, credentials or payment automation.

## Checks on October 27, 2026

- Gemini CLI 0.25.0 native extension validation passed using Node.js 24.22.1.
- All five skill frontmatter/name checks passed, and all local reference links resolved.
- All five skill directories passed the Hermes community security guard with zero findings and no override, using [upstream source](https://github.com/NousResearch/hermes-agent/tree/9af19cacdeaf5680a98aa75fad49433dcbcbe531). This scanner result is separate from Gemini runtime compatibility.
- The configured Streamable HTTP and OAuth fields were checked against Gemini's current documentation and installed CLI types.
- Postedly's public OAuth discovery metadata advertises dynamic client registration, public clients, S256 PKCE and the three requested scopes.

These checks validate the bundle's structure and advertised authentication parameters. They do not establish that sign-in and a connected tool call succeed in a clean Gemini CLI installation. No authenticated Gemini tool call, payment or physical send was part of these checks. Gallery inclusion is separate from public repository availability.

## Platform documentation

- [Extension format](https://geminicli.com/docs/extensions/reference/)
- [Remote MCP and OAuth](https://geminicli.com/docs/tools/mcp-server/)
- [Gallery discovery and releases](https://geminicli.com/docs/extensions/releasing/)

## Product documentation

- [Postedly agent guide](https://postedly.com/agent-guide.md)
- [Postedly developer guide](https://postedly.com/developers)

Original material and adaptations are licensed under the included MIT license, copyright 2026 Soxoa LLC.
