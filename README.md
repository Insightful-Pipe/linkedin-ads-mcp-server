# LinkedIn Ads MCP Server by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/linkedin-ads)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect LinkedIn Ads to AI assistants for B2B advertising analytics and campaign optimization.**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — The LinkedIn Ads MCP server enables Claude, ChatGPT, Cursor, and other AI assistants to analyze your LinkedIn advertising campaigns. Optimize B2B marketing, track lead generation, and get AI-powered recommendations.

[![Explore All MCP Servers](https://img.shields.io/badge/Explore_All-MCP_Servers-blue?style=for-the-badge)](https://insightfulpipe.com/mcp-servers)

![LinkedIn Ads MCP Server](https://insightfulpipe.com/images/linkedin-app-icon.svg)

## MCP Server URL

```
https://linkedin-ads.insightfulmcp.com/
```

## What is LinkedIn Ads MCP?

LinkedIn Ads MCP is a **remote Model Context Protocol server** that connects your LinkedIn Campaign Manager to AI assistants. This B2B-focused integration allows you to:

- Query LinkedIn ad performance using natural language
- Analyze audience targeting effectiveness
- Track lead generation and conversion metrics
- Get AI recommendations for campaign optimization
- Access demographic and creative analytics

## Installation

### Claude

1. Copy the MCP Server URL: `https://linkedin-ads.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** on the connector to start authorization
6. Click **Authorize access** in the browser to complete the connection

### ChatGPT

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://linkedin-ads.insightfulmcp.com/`
3. Authorize with your InsightfulPipe account

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http linkedin-ads https://linkedin-ads.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "linkedin-ads": {
      "url": "https://linkedin-ads.insightfulmcp.com/"
    }
  }
}
```

Then authorize the connection when Cursor prompts you.

## Available Actions

28 actions: 18 read, 10 write.

### Read Actions (18)

| Action | Description |
|--------|-------------|
| `get_account_analytics` | Retrieve analytics for the entire ad account |
| `get_accounts` | List all ad accounts accessible to the authenticated user |
| `get_analytics` | Retrieve analytics/performance data for campaigns or creatives |
| `get_budget_pricing` | Get bid pricing insights based on targeting criteria |
| `get_campaign` | Fetch details for a single campaign |
| `get_campaign_analytics` | Retrieve analytics grouped by campaign |
| `get_campaign_group` | Fetch details for a single campaign group |
| `get_campaign_group_analytics` | Retrieve analytics grouped by campaign group |
| `get_campaign_groups` | List campaign groups for an ad account |
| `get_campaigns` | List campaigns for an ad account |
| `get_conversions` | List conversion tracking rules for an ad account |
| `get_creative` | Fetch details for a single creative |
| `get_creative_analytics` | Retrieve analytics grouped by creative |
| `get_creatives` | List creatives for an ad account |
| `get_demographic_analytics` | Retrieve analytics grouped by member demographics |
| `get_lead_forms` | List lead generation forms for an ad account |
| `get_revenue_analytics` | Retrieve revenue attribution metrics (ROAS, closed opportunities, etc.) |
| `get_tracking_params` | Get UTM tracking parameters for a campaign |

### Write Actions (10)

| Action | Description |
|--------|-------------|
| `create_campaign` | Create a new campaign |
| `create_campaign_group` | Create a new campaign group |
| `create_creative_inline` | Create a creative with an inline ad post |
| `create_lead_form` | Create a Lead Generation form |
| `finalize_video_upload` | Finalize a chunked video upload |
| `initialize_image_upload` | Initialize an image upload |
| `initialize_video_upload` | Initialize a video upload |
| `update_campaign` | Partial update of a campaign |
| `update_campaign_group` | Partial update of a campaign group |
| `update_creative` | Partial update of a creative |

## Usage Examples

### Campaign Performance

```
"How are my LinkedIn ad campaigns performing this quarter?"
```

### Audience Analysis

```
"Which industries have the lowest cost per lead?"
```

### Lead Generation

```
"Show me lead form performance for my latest campaigns"
```

### Demographic Insights

```
"What job titles are converting best on my LinkedIn ads?"
```

### Budget Optimization

```
"Which campaigns should I allocate more budget to?"
```

## Supported Metrics

| Metric | Description |
|--------|-------------|
| Impressions | Total ad views |
| Clicks | Total ad clicks |
| CTR | Click-through rate |
| CPC | Cost per click |
| CPL | Cost per lead |
| Lead Form Opens | Users who opened lead forms |
| Lead Form Submissions | Completed lead forms |
| Social Actions | Likes, comments, shares |

## Why LinkedIn Ads MCP?

### For B2B Marketers
- **Professional targeting** - Analyze job-based targeting
- **Lead quality insights** - Beyond just volume

### For Demand Generation
- **Cost optimization** - Reduce CPL efficiently
- **Channel comparison** - LinkedIn vs other channels

### For Agencies
- **Multi-account management** - Handle B2B clients
- **Reporting automation** - Generate client reports

## Security & Privacy

- **Official LinkedIn Marketing API** - Direct integration with LinkedIn's API
- **OAuth 2.0** - Secure LinkedIn authentication

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers for marketing and analytics.

### Advertising MCP Servers
- [Google Ads MCP](https://insightfulpipe.com/mcp-servers/google-ads) - Search advertising
- [Facebook Ads MCP](https://insightfulpipe.com/mcp-servers/facebook-ads) - Social advertising
- [Microsoft Ads MCP](https://insightfulpipe.com/mcp-servers/microsoft-ads) - Bing advertising

### B2B Tools
- [Enrichment MCP](https://insightfulpipe.com/mcp-servers/enrichment) - Lead enrichment
- [Google Analytics MCP](https://insightfulpipe.com/mcp-servers/google-analytics) - Website analytics

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs/connectors-linkedin-ads)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
