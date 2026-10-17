# Repolex Knowledge Graph of lucidrains/denoising-diffusion-pytorch

RDF knowledge graph data for [lucidrains/denoising-diffusion-pytorch](https://github.com/lucidrains/denoising-diffusion-pytorch), parsed by [repolex](https://repolex.ai).

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
rlex download lucidrains/denoising-diffusion-pytorch
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c8155b1dc622e3f1ef0d53dc6e5a570ca105bcec
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c8155b1dc622e3f1ef0d53dc6e5a570ca105bcec
│           └── chunk-001.nq.gz
├── blob
│   ├── 069f25f8fcc78331666d9c23ed515793c513af9f.nq.gz
│   ├── 175487c1c6f6408509f15d930b9e48945125a75e.nq.gz
│   ├── 1cceeb4c8d1e0b0dd84a9f0d9a243e39f5168589.nq.gz
│   ├── 271d459f13e8ebd9ab2e404c8613b54df3f6c95a.nq.gz
│   ├── 2ca64957c7c6129b50bafc9ac8fa2f0b6cdf856f.nq.gz
│   ├── 483ea03b34dda0cb9664fdb02117ef01270fc238.nq.gz
│   ├── 5a5af2e3b45348f52b3bcd0fc518fa7a4a7fa209.nq.gz
│   ├── 667dd50f7e3ee797174f32a7925ecc192bded45e.nq.gz
│   ├── 69b9d26e4778603bca03307404f4e16cd1070185.nq.gz
│   ├── 6ec85d6199ec784a893f389b0801457ab028bdcb.nq.gz
│   ├── 82a5ea45dd140fee6aa2007ab30a9be00fec9c47.nq.gz
│   ├── 88e2cf7b5363a8a369d68cac9e5543ae97c39b7c.nq.gz
│   ├── 94c0f8a0162a77104322217c58a0122c1f1dbb77.nq.gz
│   ├── 94f335d411850771974fdd49b509f0c600bae260.nq.gz
│   ├── 958f0ec3193ba5b6bace176c76b99fe302debdba.nq.gz
│   ├── a16337c03f8bad0c723f8e562db367011ec168ed.nq.gz
│   ├── bbc1b01356b1cb9f68a223b1de8057bfed67d2fb.nq.gz
│   ├── c87f08956ad3f4fa3e5fe44d7f1c6428ab581c8f.nq.gz
│   ├── cad43213602892aadc2290cca7afa74cc9f6af64.nq.gz
│   ├── e506efc05ceac755364d0d3b6ca5ae4754f515c2.nq.gz
│   ├── e70f9323753a352ad41c844eec62515629a76272.nq.gz
│   ├── e929382bc0cc44a3e1b3b64442142672c0e07222.nq.gz
│   ├── ebda7e60b0d7eaa1480b37dca62d7a89c58c4a35.nq.gz
│   ├── f8e411f77120cee278818585d5adbf391733f562.nq.gz
│   └── fe7b383bf70bc914f2d8ba8d2d2773a76374fd37.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c8155b1dc622e3f1ef0d53dc6e5a570ca105bcec.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[lucidrains/denoising-diffusion-pytorch](https://github.com/lucidrains/denoising-diffusion-pytorch)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
