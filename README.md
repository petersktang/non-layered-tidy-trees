Code accompanying the paper "Drawing Non-layered Tidy Trees in Linear Time"

### Introduction
TreeNode contains the source Tree
Paper.Tree is the Ploeg structure supporting the algorithm.

#### Within doLayout
. TreeNode::layer() setups the y-coordinates, 
. convert from TreeNode into a type erased Ploeg tree structure.
. Marshall::runOnConverted(type erased Ploeg tree) calculates all x-coordinates based on Paper::layout()
. all x-coordinates calculated are then updated back to TreeNode from the type erased Ploeg tree
. TreeNode::normalizes move tree including subtrees recursively based on minX.
