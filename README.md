# AgentLang

A declarative cognitive orchestration language for systematic problem-solving.

## Overview

AgentLang is a file-centric strategy language that codifies HOW to explore and solve problems through structured cognitive operations. It orchestrates thinking patterns through verbs like `breakdown`, `act`, `evaluate`, and `select`, with all state externalized as immutable artifacts.

## Key Features

- **Declarative Syntax**: Describe HOW to think, not WHAT to think
- **Atomic Operations**: Each verb execution produces exactly one artifact
- **Immutable State**: All outputs are versioned files in `./artifacts/`
- **Functional Composition**: Chain verbs for complex dataflow pipelines
- **Built-in Monitoring**: Cross-platform observability binaries included

## Core Verbs

- `breakdown:` - Decompose problems (parallel/tree/rootcause)
- `act:` - Create concrete implementations (draft/rewrite/implement)
- `evaluate:` - Assess and measure (vote/test/simulate)
- `select:` - Make deterministic choices (filter)

## Example

```agentlang
baseline = breakdown:rootcause(problem.txt)
strategies = breakdown:parallel(baseline)
plan = breakdown:tree(strategies[0])
solution = act:implement(plan)
```

See `agentlang_discipline.md` for complete execution rules and verb specifications.
