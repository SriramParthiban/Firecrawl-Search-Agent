# 🔥 Firecrawl Search Agent

> 📝 Inspired by a [Nate Herk YouTube tutorial](https://www.youtube.com/@nateherk). Full credit goes to him.  

This project contains an **n8n workflow** that turns natural language queries into advanced Firecrawl `/search` requests.  
The agent can search the entire web with full control over:

- ✅ Query operators (`site:`, `intitle:`, `inurl:`, `-exclude`, etc.)  
- ✅ Filters (time-based, location, language, country)  
- ✅ Scraping formats (`markdown`, `HTML`, `JSON`, `links`, `screenshots`)  
- ✅ Included/Excluded domains  
- ✅ Full-page screenshots & structured content extraction  

---

## 🚀 Features
- Converts **plain text queries** into Firecrawl-compatible search queries  
- Supports **exclusion rules**, **site targeting**, and **title/URL filters**  
- Scrapes results in **multiple formats** for downstream AI workflows  
- Works seamlessly inside **n8n** with **OpenAI (via OpenRouter)**  

---

## ⚙️ Setup
1. Clone this repo and import the JSON workflow into **n8n**.  
2. Add your **Firecrawl API Key** under **HTTP Header Auth** credentials.  
3. (Optional) Add your **OpenRouter API key** for the LLM agent.  
4. Trigger the workflow via **chat input** or manual execution.  

---

## 🧠 Example Queries
```json
{
  "query": "Nate Herk -site:linkedin.com",
  "limit": 5
}
