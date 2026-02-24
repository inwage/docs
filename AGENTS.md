# Documentation project instructions

## About this project

- This is the Bitwage Partner API documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- API reference is auto-generated from `api-reference/openapi.yaml`
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## Terminology

- Use "user" for individual Bitwage accounts
- Use "company" for business Bitwage accounts
- Use "worker" for users invited to a company
- Use "recipient" for company-linked workers or vendors
- Use "payer" or "external payer" for external employers/clients
- Use "distribution" for payment destination configuration
- Use "funding account" for virtual bank accounts
- Use "payroll" for payment batches

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references
- Use `snake_case` for API field names in documentation

## Content boundaries

- Document only the Partner API (public-facing endpoints)
- Do not document internal admin endpoints or private API
- Do not include internal implementation details or database schemas
- Keep code examples focused on curl and common languages (Python, JavaScript)
