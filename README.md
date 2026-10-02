# Repolex Knowledge Graph of NousResearch/hermes-plugin-holographic

RDF knowledge graph data for [NousResearch/hermes-plugin-holographic](https://github.com/NousResearch/hermes-plugin-holographic), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/hermes-plugin-holographic
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   ├── 062762ab1e67dd2eeb5500dfd38785b93cb9b0e8
│   │   │   └── chunk-001.nq.gz
│   │   └── 246d9c723a79ea07bd7455bf4b364b44269526cf
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   ├── 062762ab1e67dd2eeb5500dfd38785b93cb9b0e8.nq.gz
│   │   └── 246d9c723a79ea07bd7455bf4b364b44269526cf.nq.gz
│   └── repolex
│       ├── 062762ab1e67dd2eeb5500dfd38785b93cb9b0e8
│       │   └── chunk-001.nq.gz
│       └── 246d9c723a79ea07bd7455bf4b364b44269526cf
│           └── chunk-001.nq.gz
├── blob
│   ├── 00f2d38d8063d0c6b219c0081e51888063b0c55e.nq.gz
│   ├── 021a196bd5cd2ceb53a1e57871eafc147b21dfdb.nq.gz
│   ├── 05176df2ec33233225b558d3fa727a19376b15f3.nq.gz
│   ├── 1383e942bcb2405dfa81bd54d9c301b44a7a5803.nq.gz
│   ├── 27fa77bc2949c992f639c0f4b786f78dc81c6eaf.nq.gz
│   ├── 4020728b90479ed2a4baf49b949c625696885adb.nq.gz
│   ├── 43e1f22ff8ef80885e3ff38886d7cc4ac1f4ee80.nq.gz
│   ├── 5cad6f33abbf05a4e4892c3438d4bab6b17fe789.nq.gz
│   ├── 5f58193d095b5c4c629a5d1422fd21a34745ed0c.nq.gz
│   ├── 63f678673507bc3652c8fd69d0e36b2080b65338.nq.gz
│   ├── 75410e73319c72cd3e991a501c5455eb78f38375.nq.gz
│   ├── 7e023e5fdad5dfebc8aa8751dd8164e17c05a41c.nq.gz
│   ├── 8a4ee6707048d27f5560e17e234b8bbccc19a95e.nq.gz
│   ├── 924fd8f7f48938be87ee03bb76bb93f8ac5b8f72.nq.gz
│   ├── a913cf2d394a1f452674a64b60de0589e6e423d6.nq.gz
│   ├── ae7d78f8daed3d88133f4b8587179c2314802b38.nq.gz
│   ├── aede5a1323e1f3fe5009fb41e2f19ac80dbc3cdd.nq.gz
│   ├── c28dde0960a6b839912da3fd93415a1066583636.nq.gz
│   ├── c835f01aad0284fc32a0fb26e57356866d9c9c79.nq.gz
│   ├── d5fca8707746db69b84b5f1a936e01b3ae736b5c.nq.gz
│   ├── df32a5d5123085a6ea66f673087ce1f5e92a4383.nq.gz
│   ├── e51f120bb2a8b7ff4fd0171345ce4b8de85625c6.nq.gz
│   └── ed06ca716e5f600858e94fded8d08678d7c1f9fa.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   ├── 062762ab1e67dd2eeb5500dfd38785b93cb9b0e8.nq.gz
│   └── 246d9c723a79ea07bd7455bf4b364b44269526cf.nq.gz
├── filetree
│   ├── 062762ab1e67dd2eeb5500dfd38785b93cb9b0e8.nq.gz
│   └── 246d9c723a79ea07bd7455bf4b364b44269526cf.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

16 directories, 37 files
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

[NousResearch/hermes-plugin-holographic](https://github.com/NousResearch/hermes-plugin-holographic)

---
*Parsed on 2026-10-02 by [repolex](https://repolex.ai)*
