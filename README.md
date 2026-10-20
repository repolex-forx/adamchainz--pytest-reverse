# Repolex Knowledge Graph of adamchainz/pytest-reverse

RDF knowledge graph data for [adamchainz/pytest-reverse](https://github.com/adamchainz/pytest-reverse), parsed by [repolex](https://repolex.ai).

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
rlex download adamchainz/pytest-reverse
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 84670881ea453eda1be40e475a93663ce3f05faf
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 84670881ea453eda1be40e475a93663ce3f05faf
│           └── chunk-001.nq.gz
├── blob
│   ├── 19c6f4d68b9393b18cf54cb211767c261d206fec.nq.gz
│   ├── 1cc8215bfde3e5fde2e8958b4da56ae8e858adde.nq.gz
│   ├── 205ab9ad9df4ab629d1b7b8d8a72b41f44d8824c.nq.gz
│   ├── 22ddbb118475b52ce8ecba56d9ec45009923da58.nq.gz
│   ├── 2a7f84f54867d02714727f82eef95d3be939d666.nq.gz
│   ├── 2f2f8df2fdac43ceed6fe8f8df88b0787d806da0.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 40c1340c5e19a33ea6030dd19e4c417b1989b762.nq.gz
│   ├── 40f4ac757715bb1a8c355eda9124141fdda3aeff.nq.gz
│   ├── 47ceefdbffe4e1f2a7c3c552ef51d340a0fd3991.nq.gz
│   ├── 7f1d007c01048570d774e58f46203d3e92056c39.nq.gz
│   ├── 93acb639926ccf42e9a2f76f02419eeaf0405c3a.nq.gz
│   ├── a09e8ca3cf60f61f34ab7edd7c7562781fb57812.nq.gz
│   ├── a26783c93dbdb77b22e479781ba78b41858cc3fc.nq.gz
│   ├── cbe1d62d353e1468867c1ac699e6a64411e200d3.nq.gz
│   ├── cd6cb7d8d24dcee4291529a321d2fc9fa6ca63ee.nq.gz
│   ├── db8216c6d9b966208a92d3216b82a87c5dd2f758.nq.gz
│   ├── e4857d2f488b8f9cc99fd8730409536d98eb8c3e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f0b4e5d4848bd1afeae5f01701d3634211375990.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 84670881ea453eda1be40e475a93663ce3f05faf.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 27 files
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

[adamchainz/pytest-reverse](https://github.com/adamchainz/pytest-reverse)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
