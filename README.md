# Market Research Plugin for Claude

A Claude plugin of four skills for market research and business intelligence:

| Skill | Use it for |
|---|---|
| `market-research` | Market size (TAM/SAM/SOM), CAGR, segmentation, trends, market entry |
| `competitor-intel` | Competitor discovery, feature and pricing comparison, SWOT, positioning |
| `opportunity-finder` | Ranked business opportunities with an explainable scoring model |
| `report-generator` | Full cited research reports with methodology and confidence ratings |

## Install

From a local clone:

```bash
claude plugin install ./market-research-plugin
```

Or from GitHub once published:

```bash
claude plugin install github:resuhailnawaz/market-research-plugin
```

## Example prompts

- "Size the market for accounting software for freelancers in India."
- "Compare the top five project management tools on features and price."
- "Find underserved niches in online tutoring for school students."
- "Write a research report on the EV charging market in Bihar, with sources."

## Principles

- Every number has a source or is labeled as an estimate with its formula.
- Scores and rankings show their weights and evidence.
- Only public information is used. No scraping of private data, no personal contact harvesting.
- Limitations and confidence levels are always stated.

## Repository layout

```
.claude-plugin/plugin.json     Plugin manifest
skills/<name>/SKILL.md         One folder per skill
.github/workflows/validate.yml Basic structure check on every push
README.md
LICENSE
```

## Contributing

Open an issue or pull request. Keep each skill focused on one job, and keep the description field accurate, since it decides when the skill is used.

## License

MIT
