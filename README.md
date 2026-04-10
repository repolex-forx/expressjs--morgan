# Repolex Knowledge Graph of expressjs/morgan

RDF knowledge graph data for [expressjs/morgan](https://github.com/expressjs/morgan), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download expressjs/morgan
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c1c7f107d2b58d4b9af655b7347cfe29815a897c
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── c1c7f107d2b58d4b9af655b7347cfe29815a897c.nq.gz
│   └── repolex
│       └── c1c7f107d2b58d4b9af655b7347cfe29815a897c
│           └── chunk-001.nq.gz
├── blob
│   ├── 0e064f47bff27efdbdb6abc4063f834b7ea6a0b5.nq.gz
│   ├── 1eece14ad8cb98de2093fac5eef5ccee89472ff8.nq.gz
│   ├── 3fefed9d26fb932c719530cf883d68b296293ada.nq.gz
│   ├── 54abc240ebd344279e0dbdd29930b2e454e16235.nq.gz
│   ├── 76b1021d09a5774679c815f83d1c9a4bccf21c28.nq.gz
│   ├── 8168e75b39eb6b4d583c14ec32aeb435ac6873b4.nq.gz
│   ├── 817cc7136d5aeb1bc9db1f2f2a67a7786238a4eb.nq.gz
│   ├── 9808c3b2b6602da61eb4afcb4caf33368e3e2bd4.nq.gz
│   ├── b33c4f2fd29335a7a32a030c5bf161bac4fb96cf.nq.gz
│   ├── cb39cd8d71d725ab62ebceb339dbbfc70bf6fd85.nq.gz
│   ├── cc15ef79e3c0f409f3313d9cd26219a04700ad56.nq.gz
│   ├── cc6379790c67810fb0a9e3dd7099dee55d4dd058.nq.gz
│   ├── d0682d45b39aaf4ce5e816695f3b6c756440f697.nq.gz
│   ├── dc5519c3432d3b300412464cd3bced27956a1a75.nq.gz
│   ├── f15b98e249d653f23d7e121037bde0eae1817582.nq.gz
│   └── fb6c3102d4873f71f182a336dfaa91e852a0e01f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── c1c7f107d2b58d4b9af655b7347cfe29815a897c.nq.gz
├── filetree
│   └── c1c7f107d2b58d4b9af655b7347cfe29815a897c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 26 files
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

## Source repository

[expressjs/morgan](https://github.com/expressjs/morgan)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
