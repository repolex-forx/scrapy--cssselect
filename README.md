# Repolex Knowledge Graph of scrapy/cssselect

RDF knowledge graph data for [scrapy/cssselect](https://github.com/scrapy/cssselect), parsed by [repolex](https://repolex.ai).

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
rlex download scrapy/cssselect
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 805705c5a204721d3c486250377a756bd6fa54a5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 805705c5a204721d3c486250377a756bd6fa54a5
│           └── chunk-001.nq.gz
├── blob
│   ├── 0883f0a26911303ebe4c2648b3509fd73dc2bd78.nq.gz
│   ├── 08b247756216e443b3f7891bfd38546f0d5687d0.nq.gz
│   ├── 1d5b49c7e926f690293f34848b08b501bcbc41bb.nq.gz
│   ├── 2f9ba23b8f42256c6753701155356353b07b6fa7.nq.gz
│   ├── 38558bf3772264eefb5473229510501d347c7d5b.nq.gz
│   ├── 396e0792ede9558f733f558d37f432eb97fa0e79.nq.gz
│   ├── 40335221a37ff5e8c8cf466035499b4bbdbf45c6.nq.gz
│   ├── 4f0a845ab117819fcd42a3028b4bb5a91ee83570.nq.gz
│   ├── 57b9884f7fe297560152bbfbc8a5f951831df449.nq.gz
│   ├── 623d48cfa6b6f2ba551dde2435254ed5a1b63862.nq.gz
│   ├── 664fbf61f82e51df9db8b232a7f45da9cc7780e1.nq.gz
│   ├── 66dcc22b147c711643571b56db2317e418e3905e.nq.gz
│   ├── 6b2f6af8b890374ac37678bbbbd93af86170c2ac.nq.gz
│   ├── 8125888814af6055619198304aed34094d440af9.nq.gz
│   ├── 820e1b792100da46c1b0392540e68fe85edcfe9f.nq.gz
│   ├── 91de3fef9947ea2e3c0f3f1ba1f09d6ace3ca80a.nq.gz
│   ├── a71d108a66687bf4ee107d06d5ba8787d40a63b2.nq.gz
│   ├── b91642ab9c1e3b20ad18d2430050667789bad6a0.nq.gz
│   ├── bb4f6e14dcfe77062a93b3a69a4ee80124c440e6.nq.gz
│   ├── c05529505286f030f7e7f62e80ba53c9899827ee.nq.gz
│   ├── c2183aa30a00fc473754959cf6df38391bdb481e.nq.gz
│   ├── c276bd1a74e005ed976395a5efe9cb2baa6bef17.nq.gz
│   ├── d5d9ec7061b093110dabb5836cc4b5a429891502.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efc5848fa9ad478ff4c2afd973af2aa5676b551f.nq.gz
│   └── fe96d4db080a7a60eb015ea5f71a2785f4b5e017.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 805705c5a204721d3c486250377a756bd6fa54a5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[scrapy/cssselect](https://github.com/scrapy/cssselect)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
