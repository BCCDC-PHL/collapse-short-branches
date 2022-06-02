# collapse-short-branches

This script assists in the identification of genomic clusters in newick-format phylogenetic trees using [TreeCluster](https://github.com/niemasd/TreeCluster)

It performs the following transformations on the tree:

1. Collapse all branches shorter than `--minimum_branch_length` (default 0.000001) down to zero.
2. Re-order the nodes of the tree in descending order by:
    1. Number of descendants
    2. Edge length
    3. Label
3. Resolve polytomies

## Usage

```
collapse_short_branches.py <tree.nwk> [--min_branch_length BRANCH_LENGTH] [--scale SCALE_FACTOR]
```

The collapsed tree will be printed to standard output. It can be redirected into a file using the output redirection `>` operator.
