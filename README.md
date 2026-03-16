
# Web Search API

## APIs

### Web Search

```
GET https://web-search-cat.lessx.xyz/search?q=<query>&max=<10|20>
```

| Parameter | Required | Description |
|-----------|----------|-------------|
| `q`       | Yes      | Search query |
| `max`     | No       | Number of results, `10` or `20` (default `10`) |

**Response:**

```json
{
  "query": "cloudflare workers",
  "count": 3,
  "results": [
    {
      "title": "Cloudflare Workers",
      "url": "https://workers.cloudflare.com/",
      "description": "Build serverless applications..."
    }
  ]
}
```

### News Search

```
GET https://web-search-cat.lessx.xyz/news?q=<query>&max=<10|20>
```

| Parameter | Required | Description |
|-----------|----------|-------------|
| `q`       | Yes      | Search query |
| `max`     | No       | Number of results, `10` or `20` (default `10`) |

**Response:**

```json
{
  "query": "cloudflare",
  "count": 3,
  "results": [
    {
      "title": "Cloudflare announces new feature",
      "url": "https://example.com/article",
      "source": "TechNews",
      "date": "2 hours ago"
    }
  ]
}
```

### Error Responses

- `400` - Missing required query parameter `q`
- `404` - Unknown endpoint
- `500` - Internal server error

```json
{
  "error": "Missing query parameter: q"
}
```

## MCP/SKILL
> [!TIP]
> Feel free to use [mcp-workspace](https://github.com/larryteal/mcp-workspace) to convert APIs to MCP, or simply let AI help you write a SKILL.




