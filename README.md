# Repolex Knowledge Graph of ros-infrastructure/rosdoc_lite

RDF knowledge graph data for [ros-infrastructure/rosdoc_lite](https://github.com/ros-infrastructure/rosdoc_lite), parsed by [repolex](https://repolex.ai).

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
rlex download ros-infrastructure/rosdoc_lite
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ddd083504c2559d2632fc1daa55796c7075528fa
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ddd083504c2559d2632fc1daa55796c7075528fa
│           └── chunk-001.nq.gz
├── blob
│   ├── 026f0901fb4d2e249782a08061f9b6a4304a25e6.nq.gz
│   ├── 05b0a548c5e840c81b85ad20a181434251cd6494.nq.gz
│   ├── 0d20b6487c61e7d1bde93acf4a14b7a89083a16d.nq.gz
│   ├── 124e9859371516101a6f7e03f61d6414bb2b6333.nq.gz
│   ├── 19c62c3159b82c90fbdd88e226916d7f4ae65da8.nq.gz
│   ├── 1a225e4b9383f67d5a7ddb836893e90b05f17b6d.nq.gz
│   ├── 1e55f9e4b9bc4ff432579063a8c190596b1977af.nq.gz
│   ├── 36bf9d4d869a3a1a973f091c638fa6367db3a266.nq.gz
│   ├── 3c8a580f1a6c236a1b66fb6438a66528e9d23bfd.nq.gz
│   ├── 487d64f1ed7efc3ecc55fc706d2fd9d0aa57afbd.nq.gz
│   ├── 49d3a9bfdbbfa2604ed82c7c942812af17c6d185.nq.gz
│   ├── 4b53114d138763d0e6cad81ce527a56529a47bbd.nq.gz
│   ├── 5174316f2a406271776eea140e260d937758c0db.nq.gz
│   ├── 7459ccda5ac039f34869d0e91e30045c48ca72f6.nq.gz
│   ├── 79fa96085d5168ed3bbc03648d7ea3b76664994e.nq.gz
│   ├── 7b64713673c22b42bb2aa844e333b0fb9dbad8e0.nq.gz
│   ├── 7db25a13689959b2f97e004e266c31e0266aba77.nq.gz
│   ├── 87e0206cd126a3b939a7255d98bf54c82f72cffe.nq.gz
│   ├── c245f9b6801fc182cdb819d550bbf85693a1d917.nq.gz
│   ├── c3a53b9c55fef2923bcd8a1f18bae096a8502e46.nq.gz
│   ├── c7fa5e562cc8840dd0ac3f0341e9b9eff991b7b2.nq.gz
│   ├── c8da13188e56cf214f8f5e4017f828a64b75f7d7.nq.gz
│   ├── cad7362fa290e4d35307c302e2f4c1fb316837e0.nq.gz
│   ├── d0f9394d30a52742ff3bc60360cb9e1405e6bcd8.nq.gz
│   ├── d919faf5a11cfded6b7e9e262c854be023697ef7.nq.gz
│   ├── da7c9b2b58c4af1595f9c2ed133719123fc19ab2.nq.gz
│   ├── dca80001867e5b4d1de71bfccb80937b957b2b71.nq.gz
│   ├── e78708e5e5b6ca0c51be70d36aaab87064377a32.nq.gz
│   ├── f95d16a020b6065cd1aaaf13da7328129d037895.nq.gz
│   ├── fa98553bfb50474c4eda03fb6712ac2ac8a1a10f.nq.gz
│   └── ffc9ef276ddeaf657fb5cd653dc591ad38569286.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ddd083504c2559d2632fc1daa55796c7075528fa.nq.gz
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

[ros-infrastructure/rosdoc_lite](https://github.com/ros-infrastructure/rosdoc_lite)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
