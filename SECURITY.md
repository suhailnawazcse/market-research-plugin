# Security Policy

## Supported versions

| Version | Supported |
|---|---|
| 0.1.x | Yes |
| < 0.1.0 | No |

## Scope

This repository contains Markdown skill files, a JSON manifest, and a GitHub Actions workflow. It does not run a server or store user data. Security concerns most likely involve:

- Instructions in a skill that could lead Claude to collect private data, bypass access controls, or act against a site's terms.
- Workflow configuration that could expose secrets or run untrusted code.
- Manifest fields that could mislead users about the plugin's source or permissions.

## Reporting a vulnerability

Please do not open a public issue for security problems. Instead:

1. Go to the repository's **Security** tab and choose **Report a vulnerability** (private security advisory).
2. Describe the issue, the affected file, and steps to reproduce.

You can expect an acknowledgment within 7 days. Confirmed issues will be fixed in a patch release, and you will be credited unless you prefer otherwise.

## Responsible use

The skills in this plugin are for public-information research. Do not use them to collect personal data without consent, to scrape sites in breach of their terms, or to make decisions about individuals without proper legal basis.
