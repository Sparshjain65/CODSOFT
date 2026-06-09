# CODSOFT
# 🔍 Competitor Analysis + Search Intent Analyzer

An AI-powered SEO intelligence tool that helps content creators, marketers,
and developers understand keyword opportunities, decode user search intent,
and benchmark their content strategy against competitors — all from a clean,
dark-themed web interface.

## 🚀 What It Does

- **Keyword Research** — Enter any topic and get keyword variations ranked
  by search volume, difficulty score, and opportunity potential with
  intent classification for each keyword.

- **Search Intent Classifier** — Paste any search query and instantly
  classify it as Informational, Navigational, Commercial, or Transactional
  with a confidence score, funnel stage mapping, and content format
  recommendations.

- **Competitor Analysis** — Enter your niche and get a side-by-side
  comparison of competitor domain authority, monthly traffic, content
  length, publishing frequency, and backlink counts.

- **Keyword Gap Finder** — Discover untapped keywords your competitors
  already rank for but you are missing, sorted by difficulty so you can
  target easy wins first.

- **URL Scraper** — Fetch any competitor URL and extract SEO signals
  including word count, heading structure, meta description quality,
  internal/external link counts, and an overall SEO health score.

## 🛠️ Tech Stack

| Layer      | Technology                              |
|------------|-----------------------------------------|
| NLP Engine | Python 3 (regex, heuristics, stdlib)    |
| Scraper    | Python 3 (urllib, HTMLParser)           |
| API Server | Node.js + Express.js                    |
| Frontend   | HTML5 + CSS3 + Vanilla JavaScript       |

## 📁 Project Structure

competitor-analyzer/
├── api/
│   └── server.js          # Express REST API (5 endpoints)
├── backend/
│   ├── nlp/
│   │   └── analyzer.py    # Keyword research, intent classification,
│   │                      # competitor simulation, gap finder
│   └── scrapers/
│       └── scraper.py     # URL fetcher + SEO signal extractor
├── frontend/
│   ├── index.html         # Single-page app shell
│   ├── css/style.css      # Dark theme UI
│   └── js/app.js          # API calls + dynamic rendering
├── package.json
├── requirements.txt
└── README.md

## ⚙️ Quick Start

# 1. Install Node.js dependencies
npm install

# 2. Start the server
npm start

# 3. Open in browser
http://localhost:3000

> Python 3 must be installed and added to PATH.

## 🔌 API Endpoints

| Method | Endpoint          | Body                   |
|--------|-------------------|------------------------|
| POST   | /api/keywords     | { "topic": "..." }     |
| POST   | /api/intent       | { "query": "..." }     |
| POST   | /api/competitors  | { "niche": "..." }     |
| POST   | /api/gaps         | { "niche": "..." }     |
| POST   | /api/scrape       | { "url": "https://..." }|
| GET    | /api/health       | —                      |

## 🧠 How It Works

The frontend sends HTTP requests to the Express API server.
The server spawns Python child processes, passes user input to the
NLP engine or scraper, collects the JSON output, and returns it
to the browser for rendering.

Browser → Node.js API → Python NLP/Scraper → JSON → Browser

## 🔮 Future Improvements

- Integrate Ahrefs / Semrush / DataForSEO for real keyword volume data
- Add spaCy or transformer-based NLP for higher intent accuracy
- Add user authentication and result history with a database
- Export results to CSV or PDF reports
- Add a Chrome extension for on-page competitor analysis

## 👨‍💻 Skills Demonstrated

- Full-stack web development (Python + Node.js + Vanilla JS)
- Natural Language Processing (intent classification, keyword extraction)
- Web scraping with robots.txt compliance
- REST API design and integration
- No-framework frontend development
