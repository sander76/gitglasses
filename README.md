# GitGlasses

Visualize git branch relationships in a commit range.

## Installation

```bash
uv sync
```

## Usage

```bash
gitglasses [--from <ref>] [--to <ref>]
```

- `--from`: Starting commit or branch (defaults to current HEAD)
- `--to`: Target branch or commit (defaults to "main")

### Examples

```bash
# Show branches from current HEAD to main (using defaults)
gitglasses

# Explicitly specify from HEAD to main
gitglasses --from HEAD --to main

# Show branches in last 5 commits
gitglasses --from HEAD --to HEAD~5

# Show branches from feature-a to main
gitglasses --from feature-a --to main
```

## Output

GitGlasses displays branches as an ASCII tree with box-drawing characters:

```
main
├── branch-a (a1b2c3d, e4f5g6h)
│   └── branch-b (i7j8k9l)
└── branch-c (m1n2o3p)
```

Each branch shows the abbreviated commit hashes of commits in the specified range.
