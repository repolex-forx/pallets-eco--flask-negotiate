# Repolex Knowledge Graph of pallets-eco/flask-negotiate

RDF knowledge graph data for [pallets-eco/flask-negotiate](https://github.com/pallets-eco/flask-negotiate), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/flask-negotiate
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9385116dbf18f16ffe55dedd9460799c36409185
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9385116dbf18f16ffe55dedd9460799c36409185
│           └── chunk-001.nq.gz
├── blob
│   ├── 0841c2e528b3fbd9afcecf4b1b63fc7c97681852.nq.gz
│   ├── 150394e934a9483e0aa5464c276c75531dd36e7f.nq.gz
│   ├── 23d1773c9bce8c85ef767ff6666d42ad93ca082b.nq.gz
│   ├── 2b1a4f0b9c203602ddb36d0d6ba3939d49e86e11.nq.gz
│   ├── 62f931de2ba07dfaa283f628d786547ad05eb2e5.nq.gz
│   ├── 69f365b98c4ae3871f361b722106f5f23a19bfc6.nq.gz
│   ├── 700cda09e3d93b3ea8f68ee3e3c10da18b0014a9.nq.gz
│   ├── 736bfed3854da0e0d86488103811404b7c0b08ab.nq.gz
│   ├── 7c69ee3e8d0fe8ddcb23e3494eda54a5c64f5ca6.nq.gz
│   ├── 7e3465c12d001438dff02514887bab9c8a7ffde3.nq.gz
│   ├── 8a05a51e8698babbed33230457f17c9073042d81.nq.gz
│   ├── bf7b494fc7044e1395c1c821f2babc309277bf78.nq.gz
│   └── cadb007a8fc704d4790b5b28d084430c35d1a345.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9385116dbf18f16ffe55dedd9460799c36409185.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[pallets-eco/flask-negotiate](https://github.com/pallets-eco/flask-negotiate)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
