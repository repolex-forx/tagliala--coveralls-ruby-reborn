# Repolex Knowledge Graph of tagliala/coveralls-ruby-reborn

RDF knowledge graph data for [tagliala/coveralls-ruby-reborn](https://github.com/tagliala/coveralls-ruby-reborn), parsed by [repolex](https://repolex.ai).

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
rlex download tagliala/coveralls-ruby-reborn
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7f6287e869f7761d75aa4d78cf91593ec7d8b7d7
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7f6287e869f7761d75aa4d78cf91593ec7d8b7d7
│           └── chunk-001.nq.gz
├── blob
│   ├── 060e1e7952671c2a2f6621c8091fe142c4889919.nq.gz
│   ├── 1bf8e3d690042b49eb7c3429d55a32ff3064a8d2.nq.gz
│   ├── 2300d395686854148117fd6a34856a2f961a7cba.nq.gz
│   ├── 23321c07d3a78a6740c10b8bf390889af83094fd.nq.gz
│   ├── 23c14305fea852fbedbfc1f3d561012665662630.nq.gz
│   ├── 277b69d66f99f7033aaaef6556dd5a6316d034a5.nq.gz
│   ├── 28b9ae72a7374dea4f37f99b467e2ddb027df4c7.nq.gz
│   ├── 369d80602f48db897e0d6a13459078e64bc6a45c.nq.gz
│   ├── 3eae006e9bafcc69ccc55f6aaa782903f3e48d01.nq.gz
│   ├── 3f8c996fcf3fa3740ffc81ba1e1d9e3396c96d7e.nq.gz
│   ├── 506cab2a3cf0c096b55f3221d32957b47092ff5e.nq.gz
│   ├── 59caba9563754fbc643522250f88eba796fe948e.nq.gz
│   ├── 5d42c4ba455d393035f3795f59f5683450730833.nq.gz
│   ├── 62f2b0faf330a324f2c47b949a37cdc2079bfc88.nq.gz
│   ├── 66c2f6d324bf546583b5f1f884cd0471ef11f9b8.nq.gz
│   ├── 6b8ea6574c6290b043484ee434bb867bc2fd35c2.nq.gz
│   ├── 6e901ccf78f4da2670a2b036152b473885685a57.nq.gz
│   ├── 746adc666631a9ea0d3196c245cb53a114007d52.nq.gz
│   ├── 814f29c73c4c647cfb6d00511370e0b37d6b2002.nq.gz
│   ├── 85cf827ba19771944477d2e1282caba2feddc4e8.nq.gz
│   ├── 99f8088be55d2d31c516aebc4121a58775054f37.nq.gz
│   ├── a6d43e333bfc95109c7c54973ed537f5a11ae167.nq.gz
│   ├── a9203f9d406c364a425fc8070f4562c9fd689496.nq.gz
│   ├── adf47fe0593cc070db3351bb31383c2fc4365ad8.nq.gz
│   ├── b5b202d043394f2ed90180076556d20ca63c6d34.nq.gz
│   ├── c32861d0325b260fde7fcf879d05116f9ed2e682.nq.gz
│   ├── d0c4bcc1cdc5ef6589c0b585fe7a3c72e0b6d58c.nq.gz
│   ├── d8316967512724fca211a3a25c5b69d821815c0d.nq.gz
│   ├── d9a187c47e69904a457df9acbb674f8025863fae.nq.gz
│   ├── dfebd4a441532cdea7eba7f10d4e6533e6300e5e.nq.gz
│   └── e40d4ebc01010dfd448b50c39e7a4164b3f254b2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7f6287e869f7761d75aa4d78cf91593ec7d8b7d7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[tagliala/coveralls-ruby-reborn](https://github.com/tagliala/coveralls-ruby-reborn)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
