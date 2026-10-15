# Repolex Knowledge Graph of astropy/sphinx-astropy

RDF knowledge graph data for [astropy/sphinx-astropy](https://github.com/astropy/sphinx-astropy), parsed by [repolex](https://repolex.ai).

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
rlex download astropy/sphinx-astropy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 638ede78f0417f024e355ac559e751d07423a138
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 638ede78f0417f024e355ac559e751d07423a138
│           └── chunk-001.nq.gz
├── blob
│   ├── 01bf87c8fefbb0c78de8b1c4b916ead0c07f5d1d.nq.gz
│   ├── 0328d98a09931bda7f633ebcf75de777858ada6a.nq.gz
│   ├── 0332badf21d04f5d32a8f95ef461c66c6e7a70ce.nq.gz
│   ├── 0e46157f452ada653a287dbb8ffb1491c59138a9.nq.gz
│   ├── 20e3047c403039205806bab7810e93ad50b4470e.nq.gz
│   ├── 2b1d4029dcb32e5b8109ef261a1195292a64e4b5.nq.gz
│   ├── 4269aa83043ebe2f8b35c58b252d4f043c7e9557.nq.gz
│   ├── 5a5239abbf78b55bd0c38d548d64f261445e7053.nq.gz
│   ├── 5c00cb8b6b2c533dfe75d0dc964f4716e4b9901c.nq.gz
│   ├── 685cf3405ad798929e9a087f9822ed3d79d26f61.nq.gz
│   ├── 702a607ee73c1b23c87967fe4fe931eea6dab316.nq.gz
│   ├── 7506ea5da2ecc4ec9c9e3fb140c4fd6420979e73.nq.gz
│   ├── 89e12b6d7d4403e6d0da5d3a211de88b0d881ab9.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── 95588ad50c727e615f52c376469014139d817a66.nq.gz
│   ├── a492bdefc73650ec71826b0ec9f905d9dc895b77.nq.gz
│   ├── a72e1a17ba387ae198e7dd99071c825610033adc.nq.gz
│   ├── a7b19ca892c706624f44abb2b245553844bb2a2e.nq.gz
│   ├── b48802aec06daee711409fb73eee5959c9f8cbe4.nq.gz
│   ├── bad7a41d3bd1b1281f01e13b4a412d6e7ec51483.nq.gz
│   ├── c94f76d5638aa813507040a97b43dbfd55d83fdf.nq.gz
│   ├── ce30b6d52b474f6e97dff03aed344c364bc2f16d.nq.gz
│   ├── d0581c0babab24d670283ad4807f455cbf60a08d.nq.gz
│   ├── e0fcb479401e800bf5c0ec7055920c14e3df3cc9.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ecbe4fc6cdd5bfffef57691bfa6029fd6d323b40.nq.gz
│   ├── f3ea583aa6a44a08198e0459961bb10b4fcf356d.nq.gz
│   ├── f5429e4ee6f6882d707b931c5f02e4a270476116.nq.gz
│   ├── f882d69c854c0927eda8ebf0fb0122fd316e737b.nq.gz
│   ├── fba16e7914846231e663345ddea18c71099fcdfc.nq.gz
│   └── ff7475198de2d589606aabb6738df51574fe6fcc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 638ede78f0417f024e355ac559e751d07423a138.nq.gz
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

[astropy/sphinx-astropy](https://github.com/astropy/sphinx-astropy)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
