# Repolex Knowledge Graph of jupyter-server/jupyter_server_terminals

RDF knowledge graph data for [jupyter-server/jupyter_server_terminals](https://github.com/jupyter-server/jupyter_server_terminals), parsed by [repolex](https://repolex.ai).

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
rlex download jupyter-server/jupyter_server_terminals
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 46563c0797a2d21526d0cc95c70dafc4e0e0440a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 46563c0797a2d21526d0cc95c70dafc4e0e0440a
│           └── chunk-001.nq.gz
├── blob
│   ├── 0559a09e0c2db88f256ca5190f5a29b3f122634c.nq.gz
│   ├── 16d481e2ae67d38a016ac8f8bd502cfe6aa1e9fe.nq.gz
│   ├── 1862a1bb954f877545bdd30eaf554d5adb2a0209.nq.gz
│   ├── 2037742d65938f39746f092e6849b1c4e6bb3d15.nq.gz
│   ├── 24695a280e9fea0a9f74a95e63d48a533a395073.nq.gz
│   ├── 2bb5b7bc601bf6dace477365bfe1d6158a816109.nq.gz
│   ├── 3668b98e02db2d01f571151ef161b650b70f8fa6.nq.gz
│   ├── 396330bb9729d2ec595617aef79fb28600d86bd7.nq.gz
│   ├── 39aa633d84dec9bc840e915d58366d1e609989fb.nq.gz
│   ├── 5295e776b63d7adfab3ddad99962cc6f81968909.nq.gz
│   ├── 5830bac17329df9649a8b0e37723a66c389c7b9d.nq.gz
│   ├── 586c16b0b9cad83f215f17778ec51c23c28baf2c.nq.gz
│   ├── 595fed11f09a3d6a7f6b0ae22ceec730ce09aa9b.nq.gz
│   ├── 5abe0200ff5c9525b7a58d4f83fc400ddcf6cdaa.nq.gz
│   ├── 60af4c5f16741c7c2fe17cdd9718ae5f6d56d8a4.nq.gz
│   ├── 6121230bd3ad227698e443568349f2f8e129db69.nq.gz
│   ├── 6538602a65194786f5c270d118fd1f82c0c66502.nq.gz
│   ├── 6540246ca7373ded715ca272f09c36d312c28d02.nq.gz
│   ├── 6f8b8d56d3490e7b7b146f977887cb886859ee02.nq.gz
│   ├── 6fcf05b4b76f8b9774c317ac8ada402f8a7087de.nq.gz
│   ├── 705bb9b1ebc5b9f756ccac381f36a8aeb144d47c.nq.gz
│   ├── 725feab5ce652dc39f3f2c77b9fd3c90bf049c65.nq.gz
│   ├── 97c80c282c39a87aed4d880c1fc638125b222a5a.nq.gz
│   ├── ad2c2cc99ac70cedcd836ef364d4366e9b517c40.nq.gz
│   ├── b21eb606f77b9cdcc7e3d029aa8ae4104c752518.nq.gz
│   ├── b907e57b32707c648a328b9a7fdac3d3d7a4d77a.nq.gz
│   ├── bd6925e5f4239c1561324d5192f41770e0d2dbf4.nq.gz
│   ├── bd9bcafef1a153fee15992df468c2369f2485b86.nq.gz
│   ├── c0bfbcc8f8a0f4449ff8c99de3b1991ef140a3c5.nq.gz
│   ├── cc094de6bc262a919a8b50faf28013da2347520d.nq.gz
│   ├── d0c3cbf1020d5c292abdedf27627c6abe25e2293.nq.gz
│   ├── dda430100ec1f581ce4b7e0ce87b8b9da3c82fdd.nq.gz
│   ├── e0e84cec87bdf12fedfc24a3331ac81d04b2fd56.nq.gz
│   ├── e10a5b4ceffe5b5c63c6305962d82d5247cccfe2.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ef9690715f21f4e687dcbf626526013c2ead833e.nq.gz
│   ├── f7bef4b91982d94eda5f4d69ee8815a6bb2195cc.nq.gz
│   └── fcdd3e88b66ec9b10362685146ef2a36088e54f3.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 46563c0797a2d21526d0cc95c70dafc4e0e0440a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[jupyter-server/jupyter_server_terminals](https://github.com/jupyter-server/jupyter_server_terminals)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
