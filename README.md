# Repolex Knowledge Graph of asimov-modules/asimov-nats-module

RDF knowledge graph data for [asimov-modules/asimov-nats-module](https://github.com/asimov-modules/asimov-nats-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-nats-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f2642496ac14f18007ac990546661426882e3119
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── f2642496ac14f18007ac990546661426882e3119.nq.gz
│   └── repolex
│       └── f2642496ac14f18007ac990546661426882e3119
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 2b00c7661aef863d29a553ceab559066a1aea46a.nq.gz
│   ├── 2b0c788e2596d934456a7ce78cc4e7f3fe40e217.nq.gz
│   ├── 58361d2b393f9ce9fbe5dbdc1b0db5277ec5b6a6.nq.gz
│   ├── 5a16fbfa8ef62e798f0aad7f0f1cd709fd0bac7a.nq.gz
│   ├── 62f4f7b69e20e652bba4fb027f8595b5c2fad899.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6f349a37abc7716bca0626acff5fa19a2986f261.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 77d6f4ca23711533e724789a0a0045eab28c5ea6.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── c5bcf5d666734e3ea38d4f43d78851d302348c2a.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── d2d774d685a805fac62723c16262a6ba9ded7549.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e70ce8d193caba3907b3a90b14ad50ed20756366.nq.gz
│   ├── eb9d32a8c146d219580be000ff0092d9d616e3b3.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f9750523f95de6d71eaafda4c62f6b02380488c6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── f2642496ac14f18007ac990546661426882e3119.nq.gz
├── filetree
│   └── f2642496ac14f18007ac990546661426882e3119.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 31 files
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

[asimov-modules/asimov-nats-module](https://github.com/asimov-modules/asimov-nats-module)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
