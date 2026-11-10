# Repolex Knowledge Graph of cowboy/javascript-sync-async-foreach

RDF knowledge graph data for [cowboy/javascript-sync-async-foreach](https://github.com/cowboy/javascript-sync-async-foreach), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download cowboy/javascript-sync-async-foreach
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 148e7fcdd3af583d7446e1fa19cab6dd5d8a200d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 148e7fcdd3af583d7446e1fa19cab6dd5d8a200d
│           └── chunk-001.nq.gz
├── blob
│   ├── 079a23afd1c61a33ebadfd73050397dd097ee22f.nq.gz
│   ├── 64c6eb8ffd969bb71440592d5bf84ac87ff2bbbc.nq.gz
│   ├── 7505716bca543d326cd00089959ed597d4aaf8fa.nq.gz
│   ├── 9ee98b00180fd1378aa63b61cda7bbd60d3c815e.nq.gz
│   ├── be18c43acf82f5274ba54cca2e7041fb48a6e048.nq.gz
│   └── f574204978cb1a78ffd3c3f24f70925f4f860edc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 148e7fcdd3af583d7446e1fa19cab6dd5d8a200d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 14 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[cowboy/javascript-sync-async-foreach](https://github.com/cowboy/javascript-sync-async-foreach)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
