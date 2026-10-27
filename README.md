![Postedly](assets/icon.png)

# Postedly for Gemini CLI

Send a US fax, letter, certified letter, postcard or handwritten card through Postedly. Gemini CLI prepares the exact content and recipient, gets a quote with a final proof, and gives you a private review link. You inspect the proof, recipient and total, approve, and pay through Postedly's hosted Stripe Checkout. Gemini CLI can then read payment and fulfillment status separately.

## Install and connect

Install this repository using Gemini CLI's extension installer:

```sh
gemini extensions install https://github.com/johnarndt/postedly-gemini-extension
```

Restart Gemini CLI after installation, then run:

```text
/mcp auth postedly
```

Sign in, verify your email and finish the final consent confirmation on Postedly's page. Return to Gemini CLI after the browser confirms the connection. Email verification is one step of that flow. No permanent API key or client secret is needed.

If you already configured an MCP server named `postedly` in Gemini CLI settings, that configuration takes precedence over the extension. Reuse your existing connection to avoid duplicate server entries.

## Try it

- "Mail this finished PDF to the address I give you. Show me the proof and total before I pay."
- "Write and prepare a certified letter to my landlord. Let me read the finished letter first."
- "Fax this form to my doctor's US fax number."
- "Show me available handwritten cards for a thank-you note."
- "Did my Postedly fax go through?"

## Included workflows

| Skill | Purpose |
| --- | --- |
| `mail-a-letter` | Regular or certified US mail from an existing PDF or a finished letter created with you |
| `fax-a-document` | Fax an exact finished PDF to a supported US number |
| `send-a-postcard` | Prepare a two-page postcard PDF against current print requirements |
| `send-a-handwritten-card` | Choose an available card, handwriting style and exact message |
| `track-postedly-orders` | Read existing order status, timeline and provider evidence |

Check the live catalog for availability, current limits and prices. The object beta uses a separate manual request; physical checks are not enabled in this extension.

## Connection and data

The extension connects only to `https://postedly.com/mcp/send` over Streamable HTTP. OAuth uses dynamic client registration and the scopes `orders:read`, `quotes:write` and `checkout:write`. The bundle contains no credentials or executable server.

For an authorized send, Postedly receives the selected PDF bytes or card message, sender and recipient details, service choices, and quote/order identifiers. A local PDF can be transferred through a single-use HTTPS upload address on `postedly.com` when needed. No file is uploaded merely by installing the extension.

Email codes and payment details stay on the browser pages. OAuth consent is not order approval. One document or card, one recipient and one approval belong to each order. Nothing is sent until you approve and pay. A paid order is not proof of sending, and a delivered fax does not mean a person read it.

## Help

[Developer guide](https://postedly.com/developers) · [Agent guide](https://postedly.com/agent-guide.md) · [Support](https://postedly.com/support) · [Privacy](https://postedly.com/privacy) · [Terms](https://postedly.com/terms) · [Refunds](https://postedly.com/refunds)

Operated by Soxoa LLC. Extension bundle licensed under [MIT](LICENSE).
