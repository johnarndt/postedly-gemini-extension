# Postedly

Use Postedly for a requested physical send or fax, or to track an existing Postedly order. The bundled skills cover mailing a letter or certified letter, faxing a PDF, sending a postcard, mailing a handwritten card, and reading order status.

The remote MCP server is named `postedly`. Use the operations it actually exposes, including any Gemini CLI namespace prefix. Start new sends with `postedly_services` and the relevant skill. Live availability, limits, prices and returned tool schemas take precedence over static examples.

Connect with `/mcp auth postedly` when needed. The user completes email verification and final consent on Postedly's browser page. An email verification success alone does not finish the connection: return to the consent page and complete its final confirmation before returning to Gemini CLI. Keep codes, tokens and private review links out of logs and public artifacts.

Prepare only the requested document or card and recipient. Upload the actual finished content. Quoting and getting the private review link do not approve, charge or send. The person reviews the exact proof, recipient and total on Postedly's page, explicitly approves, then pays through hosted Stripe Checkout. Stop at that handoff. Read existing orders before retrying any uncertain operation.

Documentation: https://postedly.com/agent-guide.md
