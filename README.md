# Product Kit Template

Auto-fetch data from CPW API and build your product on top.

### Setup and Build

1. **Use this template** - Click "Use this template" button above
2. **Add API key** - Go to Settings → Secrets → Actions, add `RAPIDAPI_KEY`
3. **Customize data source** - Edit [`scripts/api-call.js`](scripts/api-call.js) to change what you track
4. **Build your product** - Use the auto-updating [`data/events.json`](data/events.json) however you want

### What It Does

- Monitors financial industry channels for catastrophic event signals
- Fetches fresh data weekly (configurable schedule)
- Saves results to [`data/events.json`](data/events.json)
- Provides foundation for early detection tools

### Customize Your Detection

Edit [`scripts/api-call.js`](scripts/api-call.js):

```javascript
// Change these parameters:
entities: "financial custodians",        // What to monitor
topic: "cyberattack",                   // Event type (default: "catastrophic event")
industry: "finance",                    // Fixed to finance
```

Time range is configurable (max 7 days):
```javascript
startTime.setDate(startTime.getDate() - 1)  // Last 24 hours
 ```

### Build Your Tool

Use the event data to build alert systems, monitoring dashboards, notification tools, research platforms, or whatever problem you're interested in.

> [!NOTE]
> The [workflow file](.github/workflows/deploy.yml) includes commented examples for GitHub Pages deployment, Twitter integration, and Discord webhooks. Uncomment what you need.