# Documentation project instructions

## About this project

- This is the Bitwage Partner API documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- API reference is auto-generated from `api-reference/openapi.yaml`
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## Source of truth

- These docs describe the Partner API implemented in the backend repo `bitwage-api-serverless` (usually checked out next to this one at `../bitwage-api-serverless`).
- The backend code defines the behavior. Before documenting an endpoint, check:
  - the route and its auth in `partner_app/*_blueprints.py`
  - the request and response fields in `partner_app/schemas.py` (and the schemas it imports)
  - the required permission group in `partner_app/permissions.py`
  - the error codes the service raises (`code=` on `AppError` / `ForbiddenError`)
  - the webhook event types in `lib/webhook_company_lib.py`
- `api-reference/openapi.yaml` is edited by hand. The backend no longer generates OpenAPI specs or serves docs, so don't import or regenerate the spec from it.
- When a backend change alters what a partner sees, update these docs in the same feature and link the backend PR.

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
