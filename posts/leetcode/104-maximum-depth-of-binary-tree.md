## [104. Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)
Given a binary tree, find its maximum depth.

The maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.

Note: A leaf is a node with no children.

Example:
```js
Given binary tree [3,9,20,null,null,15,7],

    3
   / \
  9  20
    /  \
   15   7
return its depth = 3.
```
## solution

```js
/**
 * @param {TreeNode} root
 * @return {number}
 */
var maxDepth = function(root) {
  return root? Math.max(maxDepth(root.right),maxDepth(root.left))+1:0
};
```