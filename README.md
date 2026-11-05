# Bitwage Partner API docs

The public documentation for the Bitwage Partner API, built with [Mintlify](https://mintlify.com).

- `docs.json`: site configuration and navigation
- `index.mdx`, `quickstart.mdx`, `guides/*.mdx`: guide pages
- `api-reference/openapi.yaml`: the API reference, edited by hand

The API itself is implemented in the backend repo `bitwage-api-serverless`, under `partner_app/`. That code is the source of truth. See [`AGENTS.md`](AGENTS.md) for what to check before documenting an endpoint.

## Local development

```bash
npm install
npx mint dev            # preview at http://localhost:3000
npx mint broken-links   # check internal links
```

You can also install the CLI globally with `npm i -g mint`. If the preview fails to start, run `mint update`.

## Publishing

The Mintlify GitHub app deploys the site when changes are pushed to the default branch. Open a pull request for every change.
