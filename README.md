# WebDataTools Developer, app & research data MCP server
`webdatatools-dev-mcp`

An MCP server with 13 developer, app & research data tools for AI agents — Claude Desktop, Cursor, Cline or any MCP client. npm/PyPI/Crates package health, GitHub repo health and trending, VS Code and Chrome Web Store extensions, Google Play and App Store apps, CrossRef DOIs, openFDA recalls, iCal feeds, Shopify products, Hacker News and Stack Exchange.

**This server uses *your own* Apify API token.** Every tool call runs a [WebDataTools](https://apify.com/webdatatools) Actor under your Apify account and is billed to your Apify credit — pay per result, the price is in each tool description. Your token is only sent to Apify's API.

## Quick start

Requires Node.js 18+.

```bash
APIFY_TOKEN=apify_api_... npx -y github:paulet4a-commits/webdatatools-dev-mcp
```

Get a free token (the free plan includes monthly credit): https://console.apify.com/settings/integrations

## Claude Desktop / Cursor

Add this to `claude_desktop_config.json` (Claude Desktop) or `.cursor/mcp.json` (Cursor):

```json
{
  "mcpServers": {
    "webdatatools-dev": {
      "command": "npx",
      "args": [
        "-y",
        "github:paulet4a-commits/webdatatools-dev-mcp"
      ],
      "env": {
        "APIFY_TOKEN": "apify_api_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
      }
    }
  }
}
```

## Tools (13)

| Tool | What it does | Price (free plan) | Backing Actor |
|---|---|---|---|
| `package_health_checker` | npm, PyPI & Crates.io Package Health Checker | $0.002 / result | [Actor](https://apify.com/webdatatools/package-health-checker) |
| `github_repo_health` | GitHub Repository Health & Activity Report | $0.002 / result | [Actor](https://apify.com/webdatatools/github-repo-health) |
| `vscode_marketplace_extensions` | VS Code Marketplace Extension Scraper (installs, ratings) | $0.0015 / result | [Actor](https://apify.com/webdatatools/vscode-marketplace-extensions) |
| `chrome_web_store_extensions` | Chrome Web Store Extension Scraper (installs, ratings) | $0.0015 / result | [Actor](https://apify.com/webdatatools/chrome-web-store-extensions) |
| `google_play_scraper` | Google Play Scraper | $0.002 / app | [Actor](https://apify.com/webdatatools/google-play-scraper) |
| `app_store_lookup` | App Store (iOS) App Metadata, Ratings & Top Charts Lookup | $0.001 / result | [Actor](https://apify.com/webdatatools/app-store-lookup) |
| `crossref_doi_lookup` | CrossRef DOI & Citation Metadata Lookup | $0.001 / result | [Actor](https://apify.com/webdatatools/crossref-doi-lookup) |
| `openfda_recall_monitor` | FDA Recalls & Adverse Events Monitor (openFDA) | $0.002 / result | [Actor](https://apify.com/webdatatools/openfda-recall-monitor) |
| `ical_calendar_extractor` | iCal / ICS Calendar Feed to Events Extractor | $0.0005 / result | [Actor](https://apify.com/webdatatools/ical-calendar-extractor) |
| `shopify_products_scraper` | Shopify Store Products Scraper | $0.001 / result | [Actor](https://apify.com/webdatatools/shopify-products-scraper) |
| `hacker_news_scraper` | Hacker News Search & Front Page Scraper | $0.0005 / Story | [Actor](https://apify.com/webdatatools/hacker-news-scraper) |
| `github_trending_scraper` | GitHub Trending Repositories Scraper | $0.002 / Repository | [Actor](https://apify.com/webdatatools/github-trending-scraper) |
| `stackexchange_scraper` | Stack Overflow & Stack Exchange Q&A Scraper | $0.0005 / Question | [Actor](https://apify.com/webdatatools/stackexchange-scraper) |

## More WebDataTools MCP servers

- [webdatatools-mcp-server](https://github.com/paulet4a-commits/webdatatools-mcp-server) — the 10 most popular tools in one server
- [webdatatools-domain-mcp](https://github.com/paulet4a-commits/webdatatools-domain-mcp) — Domain & website intelligence
- [webdatatools-rag-mcp](https://github.com/paulet4a-commits/webdatatools-rag-mcp) — Web content for AI & RAG
- [webdatatools-social-mcp](https://github.com/paulet4a-commits/webdatatools-social-mcp) — Search, video & social data
- [webdatatools-leads-mcp](https://github.com/paulet4a-commits/webdatatools-leads-mcp) — Leads, jobs & company data

## License

MIT
