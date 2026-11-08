# Contributing

Thanks for helping improve the Market Research plugin.

## Ways to help

- Report a bug or an inaccurate skill output using the issue templates.
- Suggest a new skill or a change to an existing one.
- Improve the methodology, examples, or output formats in any `SKILL.md`.

## Development setup

No build step is required. The plugin is made of Markdown skill files and a JSON manifest.

```bash
git clone https://github.com/resuhailnawaz/market-research-plugin.git
cd market-research-plugin
claude plugin install ./
```

Validate locally before opening a pull request:

```bash
python3 -m json.tool .claude-plugin/plugin.json > /dev/null
for f in skills/*/SKILL.md; do
  head -1 "$f" | grep -q '^---$' && grep -q '^name: ' "$f" && grep -q '^description: ' "$f" && echo "OK $f"
done
```

## Guidelines for skills

- One skill, one job. If a skill needs to do two unrelated things, split it.
- Keep the `description` field accurate and specific. Claude uses it to decide when to load the skill.
- Every numeric example must show its source or be labeled as an estimate.
- Use only public information. Do not add instructions for scraping private data, harvesting personal contact details, or bypassing site terms.
- Keep quotations short and paraphrase by default.

## Pull requests

1. Fork the repository and create a branch from `main`.
2. Make focused changes. Update `CHANGELOG.md` under "Unreleased".
3. Run the validation commands above.
4. Open a pull request and fill in the template.

The CI workflow runs the same structural checks on every push and pull request.

## Commit messages

Use short, imperative subject lines, for example `Add pricing scenario section to competitor-intel`.

## Questions

Open a discussion or an issue. Please do not post private or confidential business data in public issues.
