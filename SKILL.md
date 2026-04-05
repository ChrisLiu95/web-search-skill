---
name: web-search
description: Search the web using Tavily API. Use when the user asks about current events, latest news, prices, weather, or anything that requires up-to-date information from the internet.
metadata:
  require-secret: true
  require-secret-description: "Enter your Tavily API key. Get a free one (1000 searches/month) at https://tavily.com"
---

# Web Search

## Instructions

When the user asks a question that requires current/real-time information from the internet, call the `run_js` tool with the following exact parameters:
- script name: index.html
- data: A JSON string with the following fields:
  - query: String. The search query based on the user's question.
  - maxResults: Number (optional). Maximum number of results to return. Default 5.

After receiving the search results, use them to provide a comprehensive answer to the user's question. Cite sources when relevant.
