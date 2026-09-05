# LeetCode 108 - Convert Sorted Array to Binary Search Tree

## Problem

Given an integer array `nums` where the elements are sorted in ascending order, convert the array into a height-balanced Binary Search Tree (BST).

A height-balanced binary tree is a tree in which the depth of the left and right subtrees of every node differs by at most one.

## Example 1

### Input

```text
nums = [-10,-3,0,5,9]
```

### Output

```text
[0,-3,9,-10,null,5]
```

### Explanation

The middle element `0` is selected as the root.

The elements smaller than `0` form the left subtree, while the elements greater than `0` form the right subtree.

One possible tree is:

```text
        0
       / \
     -3   9
     /   /
  -10   5
```

This tree is height-balanced.

## Example 2

### Input

```text
nums = [1,3]
```

### Output

```text
[3,1]
```

Another valid height-balanced BST can also be formed.

## Approach

Since the array is already sorted, the middle element can be selected as the root.

The same process is repeated recursively:

1. Find the middle element.
2. Create a tree node using the middle element.
3. Use the left half to construct the left subtree.
4. Use the right half to construct the right subtree.
5. Return the root.

Choosing the middle element keeps the resulting tree balanced.

## Algorithm

1. If the array is empty, return `None`.
2. Find the middle index.
3. Create the root using the middle element.
4. Recursively construct the left subtree from the left half.
5. Recursively construct the right subtree from the right half.
6. Return the root node.

## Complexity

* **Time Complexity:** `O(n log n)` for this slicing-based implementation.
* **Space Complexity:** `O(n)` including the recursive calls and array slices.

## LeetCode Details

**Problem Number:** 108
**Problem Name:** Convert Sorted Array to Binary Search Tree
**Difficulty:** Easy
**Topics:** Array, Binary Tree, Binary Search Tree, Recursion, Divide and Conquer

## Language

Python 3

## File

`solution.py`

## Author

T.Nandhini
