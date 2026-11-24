# JinXinCai Printing MCP server

**Answers custom roll label questions on digital vs flexo costs, FDA/EU MDR and food label compliance, materials and printer drift for US buyers and ops teams.**

A free, public [MCP](https://modelcontextprotocol.io) server from [JinXinCai Printing](https://customprintingco.com?utm_source=github&utm_medium=readme&utm_campaign=mcp): **JinXinCai Printing Label Printing Cost & Compliance Reference**. Connect it to ChatGPT, Claude or another AI assistant and it answers from JinXinCai Printing's published guides and articles, citing the page each answer comes from.

```
https://customprintingco.com/mcp
```

No sign-in, no API key, nothing to install. Listed in the [official MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers?search=com.customprintingco%2Fsite) as `com.customprintingco/site`.

## What you can ask

- "Should I print 5,000 custom roll labels digitally or with flexo, and at what quantity does flexo become cheaper?"
- "What hidden costs should I look for in a custom label quote, like plates, dies or setup fees?"
- "What does FDA require on a medical device label, and how is EU MDR labeling different?"
- "What has to appear on a cosmetic product label to be compliant in the US?"
- "My thermal label printer's print keeps shifting down the label. How do I fix the drift?"
- "How much more do compostable packaging labels cost than standard paper or film labels?"

## Tools

| Tool | What it does |
|---|---|
| `about_site` | Start here: what custom roll label and sticker printing: costs, materials, compliance database covers (Label printing costs: digital vs flexo vs offset, Medical device labeling: FDA & EU MDR, Food, beverage & cosmetic label compliance, Label materials, die-cut & finishing, Barcode and shipping label printing costs, Compostable and FSMA packaging costs, Label printer troubleshooting: shift, drift, misprints, White-label/OEM printing to your own brand artwork), who it is for (US agency print buyers and medical device, food & beverage and ecommerce ops teams sourcing custom labels), and its free calculators. |
| `search_site` | Search custom roll label and sticker printing: costs, materials, compliance library: Label printing costs: digital vs flexo vs offset, Medical device labeling: FDA & EU MDR, Food, beverage & cosmetic label compliance, Label materials, die-cut & finishing, Barcode and shipping label printing costs, Compostable and FSMA packaging costs, Label printer troubleshooting: shift, drift, misprints, White-label/OEM printing to your own brand artwork. |
| `read_page` | The full text of one JinXinCai Printing page: an article, guide, FAQ page or calculator page. |
| `ask_expert` | A question still open? With your OK, your name and email, the assistant sends it to JinXinCai Printing's specialists, and a person replies by email. |

Every tool only reads JinXinCai Printing's published pages, except `ask_expert`, which sends only what you approve.

## Connect it

**Claude** (claude.ai and desktop, every plan; Free allows one custom connector): Customize > Connectors > **+ Add** > **Add custom connector**. Name it, paste `https://customprintingco.com/mcp`, choose **No sign in**, then **Add**. In a chat: **+** > Connectors, switch it on. ([Claude help](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp))

**ChatGPT** (Pro, Business, Enterprise, Edu; web): **Plugins** > **+** > **Add custom MCP server**. Name it, paste the URL under Connection, accept the notice, **Create as a plugin**. In a new chat type **@** and pick it. ([OpenAI help](https://help.openai.com/en/articles/12584461))

**Claude Code**:
```bash
claude mcp add --transport http jinxincai-printing https://customprintingco.com/mcp
```
Or clone this repo: its `.mcp.json` connects it for the project.

**Cursor** (`~/.cursor/mcp.json`):
```json
{ "mcpServers": { "jinxincai-printing": { "url": "https://customprintingco.com/mcp" } } }
```

**VS Code (GitHub Copilot)**: Command Palette > **MCP: Add Server** > HTTP > paste the URL.

**Gemini CLI**:
```bash
gemini mcp add --transport http jinxincai-printing https://customprintingco.com/mcp
```

## Try it without an AI

```bash
curl -s https://customprintingco.com/mcp -H 'content-type: application/json' \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"search_site","arguments":{"query":"digital vs flexo labels"}}}'
```

## More from JinXinCai Printing

- Website: [customprintingco.com](https://customprintingco.com?utm_source=github&utm_medium=readme&utm_campaign=mcp)
- Questions: [customprintingco.com/contact](https://customprintingco.com/contact?utm_source=github&utm_medium=readme&utm_campaign=mcp)

Answers are general information from JinXinCai Printing's published pages.

## License

This repository (README and config) is MIT licensed. The server is operated by JinXinCai Printing.
