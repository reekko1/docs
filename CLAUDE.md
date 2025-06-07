# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Documentation Framework
This is a **Mintlify** documentation project. Mintlify is a modern documentation framework that uses MDX (Markdown + JSX) files.

## Essential Commands

```bash
# Install Mintlify CLI (required)
npm i -g mintlify

# Start development server (run from /docs directory)
mintlify dev

# Start on custom port
mintlify dev --port 3333

# Check for broken links
mintlify broken-links

# Update Mintlify CLI
npm i -g mintlify@latest
```

## Project Architecture

The documentation is organized as follows:
- `docs.json` - Main configuration file (theme, navigation, integrations)
- `index.mdx` - Homepage content
- `api-reference/` - API documentation with OpenAPI specification
- `essentials/` - Documentation writing guides
- `snippets/` - Reusable content snippets

## Key Development Notes

1. **MDX Files**: All documentation pages use `.mdx` extension, supporting both Markdown and React components
2. **API Documentation**: The `api-reference/openapi.json` file auto-generates API endpoint documentation
3. **Navigation**: Defined in `docs.json` under the `navigation` key
4. **Local Development**: Always run `mintlify dev` from the `/docs` directory where `docs.json` is located
5. **Auto-reload**: Changes to `.mdx` files automatically refresh in the browser during development

## Configuration Structure

The `docs.json` file controls:
- Site name, theme, and colors
- Navigation structure and tabs
- Logo and favicon paths
- External links (documentation, community, blog)
- API reference configuration