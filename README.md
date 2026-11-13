# SEC EDGAR Form 4 Insider Buying & C-Suite Signals Scraper

[![Run on Apify Store](https://img.shields.io/badge/Apify_Store-Run_Actor-00C853?style=for-the-badge&logo=apify)](https://apify.com/willowy_catamaran_fco/sec-edgar-form-4-insider-buying-scraper)

Extract real-time SEC Form 4 C-Suite open-market stock purchases (Code P) and sales with exact USD trade values, share prices, tickers, and domains.

---

## 1-Click n8n Workflow Template (Ready to Import)
Import directly into **n8n** (`Workflows -> Import from URL`) using:
`https://raw.githubusercontent.com/m3t4n01a/sec-edgar-form-4-insider-buying-scraper/main/n8n-workflow.json`

Or download [`n8n-workflow.json`](./n8n-workflow.json) from this repository.

## Claude Desktop / Cursor MCP Server Integration
Use this B2B intelligence engine directly inside Claude Desktop, Cursor, or Windsurf:
```json
{
  "mcpServers": {
    "sec-edgar-form-4-insider-buying-scraper": {
      "command": "npx",
      "args": [
        "-y",
        "@apify/actors-mcp-server",
        "--actors",
        "willowy_catamaran_fco/sec-edgar-form-4-insider-buying-scraper"
      ],
      "env": {
        "APIFY_TOKEN": "YOUR_APIFY_API_TOKEN"
      }
    }
  }
}
```

## Direct Synchronous REST API (cURL / Clay / Make)
```bash
curl -X POST "https://api.apify.com/v2/acts/willowy_catamaran_fco~sec-edgar-form-4-insider-buying-scraper/run-sync-get-dataset-items?token=YOUR_APIFY_API_TOKEN" \
  -H 'Content-Type: application/json' \
  -d '{"transactionType": "P", "minTransactionValueUsd": 25000, "daysBack": 3, "maxItems": 25}'
```