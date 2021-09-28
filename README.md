Code accompanying the paper "Drawing Non-layered Tidy Trees in Linear Time"

### Introduction
1. TreeNode contains the source Tree
2. Paper.Tree is the tree/data structure supporting the Ploeg algorithm.

#### Within doLayout
1. TreeNode::layer() setups the y-coordinates, 
2. convert from TreeNode into a type erased Ploeg tree structure.
3. Marshall::runOnConverted(type erased Ploeg tree) calculates all x-coordinates based on Paper::layout()
4. all x-coordinates calculated are then updated back to TreeNode from the type erased Ploeg tree
5. TreeNode::normalizes move tree including subtrees recursively based on minX.
