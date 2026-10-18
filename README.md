# Repolex Knowledge Graph of jaraco/autocommand

RDF knowledge graph data for [jaraco/autocommand](https://github.com/jaraco/autocommand), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/autocommand
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9d95de8ad227a76604a9205b5b211bc2a0576e91
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9d95de8ad227a76604a9205b5b211bc2a0576e91
│           └── chunk-001.nq.gz
├── blob
│   ├── 0276a3fae10eb367af326543bcd69e62432b2f7b.nq.gz
│   ├── 072e20973f08db8259d3a5343228c111858ad532.nq.gz
│   ├── 097e86de0720126a1390d728f7e50a4f89cac77f.nq.gz
│   ├── 1189a990793c92fea0206f5cc3b77eb7eb54189e.nq.gz
│   ├── 224c2935af6873d6a9735ec36a832c07b6373416.nq.gz
│   ├── 2570607399a3ae13cb92db65a9171d955d3248c6.nq.gz
│   ├── 27513ecf036a55be6dd673ee1904671a5052d4e3.nq.gz
│   ├── 41f86a1c2ad5a4a3a91cde54200b31cc103620f9.nq.gz
│   ├── 495fb50498655606928b1601d7816083a15eeccb.nq.gz
│   ├── 52da22ad5d7505919bcfd2858e1b699770ac4a39.nq.gz
│   ├── 688f7e05544bb5b4914d290c9bfe73bb99f4e06a.nq.gz
│   ├── 68d3f1248e36a169384243cadf93596c97787322.nq.gz
│   ├── 6cc45db66a1c1dbf1bedb993683b0700d0510643.nq.gz
│   ├── 715162ee48e088e0d623b95a4be9eb6495faabcb.nq.gz
│   ├── 73fbfca6b36927c6371839df3dfe733bebb2066f.nq.gz
│   ├── 791e1cc8c1d05f05aa72a6162c83fa13a46cb66f.nq.gz
│   ├── 816be3001c986bd37dbdf1950081c883f849bc41.nq.gz
│   ├── 8858306b1879e21db4b632a9665476310d041fd3.nq.gz
│   ├── a36380e11f49096210d93892ecda927f732a1472.nq.gz
│   ├── aa30b35c8cb9607576eb4529cc54b13051214760.nq.gz
│   ├── b49c3af060ce6326b8d91b9b73e76456ea0d9d2b.nq.gz
│   ├── c27d371e8b344621d518335cd4238b79d8617189.nq.gz
│   ├── c2d23b9b98fabdfff2939c54271250d4eedf6a8b.nq.gz
│   ├── cd192d15bf0dc7834f09135e8705990ddf3021ee.nq.gz
│   ├── d7d04873ca30c1d34192aeb5796ddf307ee6cc3e.nq.gz
│   ├── e487af27a02b4291c05b937ad517ec837cab0d27.nq.gz
│   ├── ed2f97693bdc4e84ce568ac65cd0cfb10d038481.nq.gz
│   ├── f17e3bfe635b7e34d808abf6f44539e22c0162e7.nq.gz
│   ├── f2e7888aed87393e0d0248d21fc9f87195f256ea.nq.gz
│   └── ff35524ae27242869ccdbff9251ca2a5adc3ad8e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9d95de8ad227a76604a9205b5b211bc2a0576e91.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 36 files
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

[jaraco/autocommand](https://github.com/jaraco/autocommand)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
