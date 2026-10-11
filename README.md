# Repolex Knowledge Graph of pydantic/monty-helm-chart

RDF knowledge graph data for [pydantic/monty-helm-chart](https://github.com/pydantic/monty-helm-chart), parsed by [repolex](https://repolex.ai).

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
rlex download pydantic/monty-helm-chart
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2ef57eac252d32c871470b7e733e0f40197eded8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2ef57eac252d32c871470b7e733e0f40197eded8
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b2ea44a07c02a54750f78bd13b30cbb85c70f63.nq.gz
│   ├── 0d7149dc47bb2a7dfc94d77c37a196d8a5d2fbb0.nq.gz
│   ├── 0e2fdcd48627879c3e3c0fe690c61992039db932.nq.gz
│   ├── 196fc0dda29806a029d19e17c4a250f44935c4d5.nq.gz
│   ├── 2325a84c3609887caab9a02d9bd3e3cece5db4a3.nq.gz
│   ├── 4aee271cf457827e389ced0425348bd3eb66cb93.nq.gz
│   ├── 4d21c0690197c04979735b058d2adf2fe6a52a59.nq.gz
│   ├── 61a66b40fac61bcce4c7ffe622b7b5a221b32dad.nq.gz
│   ├── 6ea7f078e3a55abef42d0f3d90e0e28459ed5aea.nq.gz
│   ├── 7a6569bcfcacbfe87999d88fbf4bedbe20fb5264.nq.gz
│   ├── 7c4d7a07bea1aa5be4e34b4f35669bce12a4a670.nq.gz
│   ├── 87d40a6cbc59684b2078ffd3b7b3d659b6714791.nq.gz
│   ├── 889c106bc776b30d4fbb199baeeb1278c197312e.nq.gz
│   ├── 8dd36ec4ac423d0b8b41baf8f4b9a38429a5f481.nq.gz
│   ├── 97aefd32b1e52b9b725051107340d6f044045bb4.nq.gz
│   ├── 9d1a8cc9db783d98c873a16086ca04e6b11cbe1f.nq.gz
│   ├── a0845bc59a03ad81f06b8a237770b0d08c2cad7b.nq.gz
│   ├── a661536eea6bcfdfe8fc0a5278b6d987a36bb410.nq.gz
│   ├── addd2f6af326425456e08c5fce02afb8531ccd09.nq.gz
│   ├── b426f5f617552b0106e540ae4e3416918c59e0ca.nq.gz
│   ├── bcf47e4a222be7632710e4ab646dca7d5c100d5c.nq.gz
│   ├── d62d376e176c3d5254e796a80bd0f356f8636052.nq.gz
│   ├── e5403301a2627be7e645ed401bc499ca605ef9ae.nq.gz
│   └── e931a3499413e5c459fbfa412f4510143f71d6ba.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2ef57eac252d32c871470b7e733e0f40197eded8.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[pydantic/monty-helm-chart](https://github.com/pydantic/monty-helm-chart)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
