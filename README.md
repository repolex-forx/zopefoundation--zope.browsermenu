# Repolex Knowledge Graph of zopefoundation/zope.browsermenu

RDF knowledge graph data for [zopefoundation/zope.browsermenu](https://github.com/zopefoundation/zope.browsermenu), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/zope.browsermenu
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 42a38908d144143bbab5408bea11f63f440baf05
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 42a38908d144143bbab5408bea11f63f440baf05
│           └── chunk-001.nq.gz
├── blob
│   ├── 188120b692cc972bed5f7063baaa7ebd9dd5fcea.nq.gz
│   ├── 35d246a34382078e3e7e2fcea97b60a4f20e512d.nq.gz
│   ├── 436b32cd04bfb088ee056e9dd321f2654d1f21b2.nq.gz
│   ├── 557cdf5e945f7ec43e186067b720b59b62b0e245.nq.gz
│   ├── 6835566dfc7e320142f4e3770fd4b680a3af798c.nq.gz
│   ├── 74223f2566ffd1b2cd151d40b275499483212c5b.nq.gz
│   ├── 79859e06010bf4967c5b4b044afea6ef39742938.nq.gz
│   ├── 7c88981e70016fa6fd2b97ea76f5378feef28d96.nq.gz
│   ├── 880477a03c2d03d9536cd89e847500fd5de68354.nq.gz
│   ├── 8a1cde635fcfe005cc4438d504940505395236a7.nq.gz
│   ├── 8baa39f053342d9c87be25d86910b3cba1389c3b.nq.gz
│   ├── 97b0a1a74e41cacf79606608f5447896b9ccd598.nq.gz
│   ├── 9954328f1910b389ad3db21e7cd1886ae5fdcd28.nq.gz
│   ├── 9eeef001b161d89aa6f75cd8d76b8179b06d3de5.nq.gz
│   ├── a3df1ed2dc539d0590216374fb1488de65c3ecc6.nq.gz
│   ├── ab8fe70ee5406e7f748cf69a26af9ffd81cec7cd.nq.gz
│   ├── ad055290734efb8636a8689d44068c8253e19827.nq.gz
│   ├── b340594d4be40113ce126163f16a911ede7b477b.nq.gz
│   ├── b3e09256097acee1f344272bb8b6151789d4e070.nq.gz
│   ├── b56c830b25d1febf50ba8d53f0f1e67329a2e31f.nq.gz
│   ├── b90ff32a4a7ab84a7d2487ef7b079a6b13b759aa.nq.gz
│   ├── bba6222a4c823889cde17b8e4205419c28e8dc06.nq.gz
│   ├── bbb41ee2e802e1689ec7164d09fedff6842124c2.nq.gz
│   ├── c9e59c5135e53f73bc1b2b5f8694cbb8e7cdfac8.nq.gz
│   ├── ca517f4eb0cec1c691c0c2b54cd5eb85e906f11b.nq.gz
│   ├── de8d6c33c0fc8cf7b851cc56841478d08abdf768.nq.gz
│   ├── e09ce4b359a7169cd601e1d61d5faee09edb923e.nq.gz
│   ├── e1f9ad7b3b48377bfbfaa1b380c384ddea24060f.nq.gz
│   ├── e4b867329e05886a4818f86b117fca2102bc84bf.nq.gz
│   ├── e66bafa424f62b83b826f64c540b9ee55231ab39.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f301aff0df2b13459e6661976de73fe498846921.nq.gz
│   ├── f8fc5bf958153d36dcb6e0e8b016361c462239e2.nq.gz
│   └── fa2d78c0801ff3e483fc6c7c90a9219c7104899c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 42a38908d144143bbab5408bea11f63f440baf05.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 42 files
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

[zopefoundation/zope.browsermenu](https://github.com/zopefoundation/zope.browsermenu)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
