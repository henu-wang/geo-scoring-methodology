# GEO Scoring Methodology

An open methodology for evaluating how well a website is optimized for AI search engines (Generative Engine Optimization).

This scoring system is used by [GEOScore](https://geoscoreai.com) to assess website readiness for AI-powered search engines like ChatGPT, Perplexity, Google AI Overviews, and Gemini.

## Why This Matters

AI search engines are fundamentally changing how people discover information. Unlike traditional search engines that rank pages in a list, AI engines:

- **Synthesize answers** from multiple sources
- **Cite specific websites** as references
- **Evaluate authority and structure** differently than Google's PageRank

Websites that aren't optimized for AI search risk becoming invisible to a growing share of search traffic.

## The 11 GEO Checks

Our methodology evaluates websites across 11 technical dimensions:

### 1. AI Crawl Access (Weight: 15%)

**What it checks:** Whether major AI search engine crawlers can access your content.

| Crawler | Operator | Product |
|---------|----------|---------|
| GPTBot | OpenAI | ChatGPT |
| OAI-SearchBot | OpenAI | ChatGPT Search |
| PerplexityBot | Perplexity | Perplexity AI |
| Google-Extended | Google | Gemini / AI Overviews |
| ClaudeBot | Anthropic | Claude |
| Applebot-Extended | Apple | Apple Intelligence |

**Scoring:**
- All major crawlers allowed: 100%
- Some crawlers blocked: Proportional deduction
- All crawlers blocked: 0%

### 2. Structured Data (Weight: 12%)

**What it checks:** JSON-LD / Schema.org markup quality and completeness.

**Key schemas evaluated:**
- `Organization` or `WebSite` on homepage
- `Article` / `BlogPosting` on content pages
- `FAQPage` for Q&A content
- `Product` for e-commerce
- `BreadcrumbList` for navigation

**Scoring:**
- Valid, comprehensive schema: 100%
- Basic schema present: 50-80%
- No schema or errors: 0-30%

### 3. llms.txt (Weight: 8%)

**What it checks:** Presence and quality of the `llms.txt` file.

**Criteria:**
- File exists at `/llms.txt`
- Contains site description
- Lists key pages with URLs
- URLs are accessible
- Content is well-structured

**Scoring:**
- Complete, well-structured file: 100%
- Basic file present: 50-70%
- No file: 0%

Learn more: [Complete llms.txt Guide](https://geoscoreai.com/blog/llms-txt-guide)

### 4. Content Structure (Weight: 12%)

**What it checks:** How well content is organized for AI extraction.

**Criteria:**
- Clear H1-H6 heading hierarchy
- Short, focused paragraphs
- Descriptive headings (not ambiguous)
- Lists and tables for structured information
- Key facts stated clearly and early
- FAQ sections with Q&A format

### 5. Meta Tags (Weight: 8%)

**What it checks:** Quality of meta information.

**Criteria:**
- Title tag (unique, descriptive, <60 chars)
- Meta description (compelling, <160 chars)
- Open Graph tags
- Twitter Card tags
- Canonical URL
- Language/hreflang tags

### 6. HTTP Headers (Weight: 5%)

**What it checks:** Server response headers.

**Criteria:**
- HTTPS enabled
- Proper content-type
- Caching headers
- Security headers (HSTS, CSP, etc.)
- Fast response time

### 7. Sitemap (Weight: 8%)

**What it checks:** XML sitemap accessibility and completeness.

**Criteria:**
- Sitemap exists and is accessible
- Referenced in robots.txt
- All important pages included
- No broken URLs in sitemap
- Proper lastmod dates

### 8. Robots.txt (Weight: 8%)

**What it checks:** Robots.txt configuration for AI crawlers.

**Criteria:**
- File exists and is valid
- Doesn't block AI crawlers
- References sitemap
- Logical allow/disallow rules

Learn more: [Robots.txt for AI Crawlers](https://geoscoreai.com/blog/robots-txt-ai-crawlers)

### 9. Citation Value (Weight: 10%)

**What it checks:** How likely AI engines are to cite your content.

**Criteria:**
- Original data or research
- Expert authorship signals
- Statistical claims with sources
- Clear, quotable statements
- Unique insights not found elsewhere

Learn more: [How to Get Cited by ChatGPT](https://geoscoreai.com/blog/how-to-get-cited-by-chatgpt)

### 10. Internal Linking (Weight: 7%)

**What it checks:** Link structure quality.

**Criteria:**
- Logical internal link structure
- Descriptive anchor text
- Hub-spoke content architecture
- No broken internal links
- Reasonable link depth

### 11. Content Depth (Weight: 7%)

**What it checks:** Comprehensive content analysis.

**Criteria:**
- Word count and depth appropriate for topic
- Topic coverage completeness
- Supporting evidence and examples
- Regular content updates
- E-E-A-T signals (expertise, experience, authority, trust)

Learn more: [E-E-A-T for AI Search](https://geoscoreai.com/blog/eeat-for-ai-search)

## Overall Score Calculation

```
GEO Score = Σ (Check Score × Weight) for all 11 checks
```

| Score Range | Rating | Interpretation |
|------------|--------|----------------|
| 90-100 | Excellent | Highly optimized for AI search |
| 70-89 | Good | Well-positioned with room for improvement |
| 50-69 | Fair | Basic optimization, significant gaps |
| 30-49 | Poor | Major issues need addressing |
| 0-29 | Critical | Essentially invisible to AI search |

## Automated Scanning

You can run all 11 checks automatically using [GEOScore](https://geoscoreai.com):

1. **Free Scan**: Instant results across all checks → [geoscoreai.com](https://geoscoreai.com)
2. **Pro Report ($29)**: Deep analysis with AI search simulation and actionable recommendations → [Pro Upgrade](https://geoscoreai.com/pro-upgrade)

## Research & References

- [GEO: Generative Engine Optimization](https://arxiv.org/abs/2311.09735) — Foundational research paper
- [What is GEO?](https://geoscoreai.com/blog/what-is-geo) — Comprehensive introduction
- [AI Search Ranking Factors](https://geoscoreai.com/blog/ai-search-ranking-factors) — What factors matter most
- [Awesome GEO](https://github.com/henu-wang/awesome-geo) — Curated resource list

## Contributing

We welcome contributions to improve this methodology. Please open an issue or submit a PR with:

- New research findings on AI search ranking factors
- Suggestions for additional checks or criteria
- Real-world data on what drives AI search citations
- Corrections or updates to existing criteria

## License

This methodology is released under the MIT License. You are free to use, modify, and distribute it.

---

*Maintained by [GEOScore](https://geoscoreai.com) — AI Search Visibility Scanner*

## All GEOScore Open Source Projects

| Project | Description |
|---------|-------------|
| [awesome-geo](https://github.com/henu-wang/awesome-geo) | Curated list of GEO resources |
| [geo-scoring-methodology](https://github.com/henu-wang/geo-scoring-methodology) | This project |
| [ai-robots-txt-generator](https://github.com/henu-wang/ai-robots-txt-generator) | Robots.txt generator tool |
| [geo-checklist](https://github.com/henu-wang/geo-checklist) | Interactive readiness checklist |
| [ai-crawlers-reference](https://github.com/henu-wang/ai-crawlers-reference) | AI crawler database |
