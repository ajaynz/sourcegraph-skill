# Sourcegraph Skills

AI agent skills for searching and understanding codebases with Sourcegraph.

## Installation

### Claude Code

```bash
bunx add-skill YOUR_GITHUB_USERNAME/skills
```

Or manually copy the `.claude/skills/` directory to your project or `~/.claude/skills/`.

### Any Agent

The skills follow the [Agent Skills](https://agentskills.io) open standard and can be used with any compatible AI agent.

## Available Skills

### searching-sourcegraph

Search Sourcegraph-indexed codebases for patterns, examples, and system understanding.

**Use when:**
- Implementing new features (find similar patterns first)
- Understanding unfamiliar code ("how does X work")
- Debugging issues (trace errors and recent changes)
- Finding examples of API usage

**Tools used:**
- `sg_keyword_search` - Exact pattern matching
- `sg_nls_search` - Semantic/concept search
- `sg_deepsearch_read` - Architectural understanding
- `sg_find_references` - Trace symbol usage
- `sg_go_to_definition` - Jump to implementations
- `sg_read_file` - Read file contents
- `sg_diff_search` - Find code changes
- `sg_commit_search` - Search commit history

## Structure

```
.claude/skills/searching-sourcegraph/
├── SKILL.md                    # Main skill instructions
├── query-patterns.md           # Regex patterns reference
├── examples/
│   └── common-searches.md      # Real-world examples
└── workflows/
    ├── implementing-feature.md
    ├── understanding-code.md
    └── debugging-issue.md
```

## License

MIT
