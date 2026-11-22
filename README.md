# Repolex Knowledge Graph of alex/rust-asn1

RDF knowledge graph data for [alex/rust-asn1](https://github.com/alex/rust-asn1), parsed by [repolex](https://repolex.ai).

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
rlex download alex/rust-asn1
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3abb539ddb67a9008050a17ca16eb65a5ad3da62
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3abb539ddb67a9008050a17ca16eb65a5ad3da62.nq.gz
│   └── repolex
│       └── 3abb539ddb67a9008050a17ca16eb65a5ad3da62
│           └── chunk-001.nq.gz
├── blob
│   ├── 19afeb634f6c7a6fbb81b1b8f4cc3e070df32f9d.nq.gz
│   ├── 19bdffdd1239332e8a6c294a951a0e10cf9f74c2.nq.gz
│   ├── 225baa1ffbcd473c70b24700c9cfd6c2f08cddf1.nq.gz
│   ├── 22761ba7ee19a94703411264d274ae1da1d326ff.nq.gz
│   ├── 23d18cc0782737d6b6ef463cc3b11e4bc1805abc.nq.gz
│   ├── 28bdbf8a81400aa4d77e7fee366a8298490a3b9a.nq.gz
│   ├── 290738c7a6c32913aee4c2dd762ab78ec94b9797.nq.gz
│   ├── 3a71567c86e1312be658ea2267051768fdbbca22.nq.gz
│   ├── 4747a02210db0088aa13dcc9ec41b0b8f1ccaf57.nq.gz
│   ├── 4f316eca8a1f68b71effc889b497b5cde652550e.nq.gz
│   ├── 572e03bdf321b6cc3a99488183436905cefd086d.nq.gz
│   ├── 5c6a058b3ac4501a605c06dc4800e81e1a60600b.nq.gz
│   ├── 69528d12f69c1580900e87d9362bc1c8130cf831.nq.gz
│   ├── 6cd4d110190f98db0be246a26d734acd55fdda4b.nq.gz
│   ├── 6ff9abbf78c4187fd4d0bd4af918bd8886b6433b.nq.gz
│   ├── 7dcbd90e11f55288c15a0d99ede56b9ea259d7bc.nq.gz
│   ├── 7f5b58e9a48fc2e8fd835b06b0c60a91f96d0983.nq.gz
│   ├── 8011e724c126515723037133d54dd3b2e79362fb.nq.gz
│   ├── 851b02fa95a32ba1d4b7ae2f706dc0f28157685a.nq.gz
│   ├── 8d818bda6dbac6fdd2556b127f5e7ebd6a17c2ba.nq.gz
│   ├── 908d517cdfff409445214b1f13e4516d90c53ace.nq.gz
│   ├── 9482224c3df6b0765d10f36e76f576c53d64cc3f.nq.gz
│   ├── 95f8e6e831c2fc6bbf4ff01571ac67108d497e28.nq.gz
│   ├── 964e468cc581fd35bdc1df3590d7084385ab9fc0.nq.gz
│   ├── 9a749089061eb94986b8833ecfe1f272b56dcec6.nq.gz
│   ├── 9fc42be332a44e1d97e83898016fcf60723f97db.nq.gz
│   ├── a49ee57dcaf9ce2540f74c5770944cf47d73571e.nq.gz
│   ├── a9d37c560c6ab8d4afbf47eda643e8c42e857716.nq.gz
│   ├── b3f5bbe0fe4744f313ba7ce6801cfbce54620106.nq.gz
│   ├── c4e1d99d56c10c3b24155a5ffe88dea33b360b7d.nq.gz
│   ├── cc52af4fb1770acfac0c7d0bb43d6afd6e38ce80.nq.gz
│   ├── dd6435f018ede37b34df488a2886e96f56d08d54.nq.gz
│   ├── e22e35f7e9dcd3838745dc522bfefe869ec04523.nq.gz
│   ├── e448d7a410f3c42bb75e1172c05617569872482b.nq.gz
│   ├── ea5b60640b01f74e295037aa8a6b7d4ea278a739.nq.gz
│   ├── f6a725f04a0f81c12ba426b038944f8d9e1b4db4.nq.gz
│   └── fc2c805f1dd68736240d31c0cd478387abd22862.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 3abb539ddb67a9008050a17ca16eb65a5ad3da62.nq.gz
├── filetree
│   └── 3abb539ddb67a9008050a17ca16eb65a5ad3da62.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 47 files
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

[alex/rust-asn1](https://github.com/alex/rust-asn1)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
