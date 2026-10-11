# Repolex Knowledge Graph of pytest-dev/pytest-print

RDF knowledge graph data for [pytest-dev/pytest-print](https://github.com/pytest-dev/pytest-print), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-print
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 514e2bcfc3497546183df2a4d18aca9b6a28c549
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 514e2bcfc3497546183df2a4d18aca9b6a28c549
│           └── chunk-001.nq.gz
├── blob
│   ├── 08473a3e72b5bc1a1a11a5b753d9e7d4dc56d00b.nq.gz
│   ├── 0a83a68d0f85612c08c6f511fab9610526610fa3.nq.gz
│   ├── 258451e6b988b4786f98b6904a67c9c3b5ef21ad.nq.gz
│   ├── 2a4f942b84b8a17e0b4d8d4316f2d7284f8384fd.nq.gz
│   ├── 3d6d206fe66858d5135e0816693a85e34d377e57.nq.gz
│   ├── 4c9959b955d5567e05d618501f573ff0a62bfceb.nq.gz
│   ├── 5e5428164d8ddaa1b2acea3adba5eed19db69d74.nq.gz
│   ├── 5f89818f9e63c2f6829c7706c57f223cdb5bbd38.nq.gz
│   ├── 69d0cfd202c019ca1d5a92d59faf9a1380c61930.nq.gz
│   ├── 7ced99896cdda11dac8879a66018560b6d999147.nq.gz
│   ├── 894546a25a0fec021597f53edc4110b403dfc2dd.nq.gz
│   ├── 8babb03aeb50f552f90c772ddc1a2f2f9c8c44c3.nq.gz
│   ├── 9daaa666b3ec380b36a7b3fd8100279175cfaac6.nq.gz
│   ├── 9fabb8f8b20ad0f75163e4da2492af1eac836ec4.nq.gz
│   ├── ae419c100b25005bd082785a7709b42a9e0300ba.nq.gz
│   ├── b2a8862a3e6ffe12e3e0575f9a311d72e941ca15.nq.gz
│   ├── c0fd26bfab64fab7b16f5ee8f66f2eadc728809d.nq.gz
│   ├── c3f349578b2797e1b7975c504ff1bac6561dbedf.nq.gz
│   ├── d2f2eac278f8e6199b473531af059e3dc248c6ff.nq.gz
│   ├── d42671c0d061a5b831ab428d6927e717264626b9.nq.gz
│   ├── d7c37e8d571b926118a4c6de9a2ac9f5ae547668.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── fd9d35f2e7d68aa969246eac2c1a809f9e9a95ef.nq.gz
│   └── fecf6a7a2d3bef333efebc7c1028bfdbad70821c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 514e2bcfc3497546183df2a4d18aca9b6a28c549.nq.gz
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

[pytest-dev/pytest-print](https://github.com/pytest-dev/pytest-print)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
