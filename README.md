# Visual Go Tutorials

Learn Go with diagrams, not walls of text.

A series of standalone visual tutorials that explain the [official Go tutorials](https://go.dev/doc/tutorial/) with inline SVG diagrams, syntax-highlighted code, and step-by-step structure. Each tutorial is a single self-contained HTML file — no build step, no dependencies.

## Tutorials

| #   | Tutorial                                                            | Status     |
| --- | ------------------------------------------------------------------- | ---------- |
| 01  | [Getting started](go-getting-started.html)                          | 🔲 Planned |
| 02  | [Create a module](go-create-module.html)                            | 🔲 Planned |
| 03  | [Multi-module workspaces](go-workspaces-tutorial.html)              | ✅ Done    |
| 04  | [Accessing a relational database](go-database-access.html)          | ✅ Done    |
| 05  | [RESTful API with Go and Gin](go-rest-api-gin.html)                 | 🔲 Planned |
| 06  | [Getting started with generics](go-generics.html)                   | 🔲 Planned |
| 07  | [Getting started with fuzzing](go-fuzzing.html)                     | 🔲 Planned |
| 08  | [Getting started with govulncheck](go-govulncheck.html)             | 🔲 Planned |
| 09  | [Vulnerable dependencies with VS Code Go](go-vulncheck-vscode.html) | 🔲 Planned |

### Bonus

| #    | Tutorial                                             | Status     |
| ---- | ---------------------------------------------------- | ---------- |
| B-01 | [Writing web applications](go-web-applications.html) | 🔲 Planned |
| B-02 | [A Tour of Go](go-tour.html)                         | 🔲 Planned |

## Live site

👉 **[visual-go-tutorials](https://arafat-al-mahmud.github.io/visual-go-tutorials/)**

## How it's built

Each tutorial is created using a Claude Project with a reference design template and project instructions that maintain consistency across the series. The design system uses:

- **DM Serif Display** for headings
- **Source Sans 3** for body text
- **JetBrains Mono** for code
- Inline SVG diagrams with a teal/purple/coral color palette
- No build tools, no JS frameworks — just HTML

## Attribution

Tutorial content adapted from [go.dev](https://go.dev/doc/tutorial/), licensed under [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/).

## License

Content: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
Code/Design: MIT
