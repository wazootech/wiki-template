# wiki-template

Generic **Wiki CLI** workspace starter — `wiki init` parity plus GitHub Pages deploy.

This is the privileged generic scaffold. For the Karpathy-pattern [LLM Wiki](https://github.com/wazootech/wiki/blob/main/docs/wiki/LLM_Wiki.md) vault (agent gardening, shapes, SPARQL indexes), use [`llm-wiki-template`](https://github.com/wazootech/llm-wiki-template) ([#83](https://github.com/wazootech/wiki/issues/83)).

Full ecosystem registry: [Wiki CLI templates](https://github.com/wazootech/wiki/blob/main/docs/wiki/Wiki_CLI.md#ecosystem-templates).

## Quick start

1. Click **Use this template** on GitHub (or clone this repo).
2. Install [Wiki CLI](https://pypi.org/project/wazootech-wiki/):

```bash
pip install wazootech-wiki
```

3. Validate and preview:

```bash
wiki check --strict
wiki serve --watch
```

4. Enable **Settings → Pages → Source: GitHub Actions** so the deploy workflow can publish `wiki build` output.

## Workspace layout

- `wiki.yaml` — config root (`wiki.inputs`, `graph.*`, `site.*`)
- `wiki/` — markdown vault with semantic frontmatter
- `layouts/` — Jinja page templates
- `assets/` — static files copied on `wiki build`

## Commands

| Command | Purpose |
| ------- | ------- |
| `wiki check` | SHACL, JSON Schema, routes, layout integrity |
| `wiki lint` | Broken links, filename pattern, heading conventions |
| `wiki fmt` | Mechanical markdown layout |
| `wiki serve --watch` | Local preview |
| `wiki build` | Static HTML for deployment |
| `wiki export` | JSON-LD, Turtle, TriG RDF serializations |

## Related

- [Wiki CLI](https://github.com/wazootech/wiki)
- [Getting started](https://github.com/wazootech/wiki/blob/main/docs/wiki/Getting_Started.md)
