# Visual Go Tutorials — Series Manifest

## Overview
A series of standalone HTML tutorials published via GitHub Pages that visually explain the official Go tutorials from go.dev. Each tutorial is a single self-contained HTML file with inline SVG diagrams, syntax-highlighted code blocks, terminal output blocks, and step-by-step explanations.

## Repo
- **Repo name**: `visual-go-tutorials`
- **Live URL**: `https://USERNAME.github.io/visual-go-tutorials/`
- **Pages config**: deploy from main branch root, `.nojekyll` disables Jekyll

## Series index

| #  | Title                                          | Official URL                                              | Filename                              | Status  |
|----|------------------------------------------------|-----------------------------------------------------------|---------------------------------------|---------|
| 01 | Getting started                                | https://go.dev/doc/tutorial/getting-started               | go-getting-started.html               | planned |
| 02 | Create a module                                | https://go.dev/doc/tutorial/create-module                 | go-create-module.html                 | planned |
| 03 | Multi-module workspaces                        | https://go.dev/doc/tutorial/workspaces                    | go-workspaces-tutorial.html           | done    |
| 04 | Accessing a relational database                | https://go.dev/doc/tutorial/database-access               | go-database-access.html               | planned |
| 05 | RESTful API with Go and Gin                    | https://go.dev/doc/tutorial/web-service-gin               | go-rest-api-gin.html                  | planned |
| 06 | Getting started with generics                  | https://go.dev/doc/tutorial/generics                      | go-generics.html                      | planned |
| 07 | Getting started with fuzzing                   | https://go.dev/doc/tutorial/fuzz                          | go-fuzzing.html                       | planned |
| 08 | Getting started with govulncheck               | https://go.dev/doc/tutorial/govulncheck                   | go-govulncheck.html                   | planned |
| 09 | Vulnerable dependencies with VS Code Go        | https://go.dev/doc/tutorial/govulncheck-ide               | go-vulncheck-vscode.html              | planned |

### Bonus (longer-form, outside the core tutorial series)
| #    | Title                     | Official URL                           | Filename                    | Status  |
|------|---------------------------|----------------------------------------|-----------------------------|---------|
| B-01 | Writing web applications  | https://go.dev/doc/articles/wiki/      | go-web-applications.html    | planned |
| B-02 | A Tour of Go              | https://go.dev/tour/                   | go-tour.html                | planned |

## Navigation link map
When a tutorial is published, these are the relative hrefs for prev/next:

| Tutorial | Prev href                      | Next href                    |
|----------|--------------------------------|------------------------------|
| 01       | (none — disabled)              | go-create-module.html        |
| 02       | go-getting-started.html        | go-workspaces-tutorial.html  |
| 03       | go-create-module.html          | go-database-access.html      |
| 04       | go-workspaces-tutorial.html    | go-rest-api-gin.html         |
| 05       | go-database-access.html        | go-generics.html             |
| 06       | go-rest-api-gin.html           | go-fuzzing.html              |
| 07       | go-generics.html               | go-govulncheck.html          |
| 08       | go-fuzzing.html                | go-vulncheck-vscode.html     |
| 09       | go-govulncheck.html            | (none — disabled)            |

## Attribution
All tutorial content is adapted from go.dev, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Each HTML file includes a license bar at the bottom.
