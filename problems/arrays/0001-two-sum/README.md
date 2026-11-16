# 1. Two Sum

**Difficulty:** Easy  
**Topics:** Arrays, hash maps  
**Problem:** [LeetCode — Two Sum](https://leetcode.com/problems/two-sum/)

## Problem summary

Given an integer array and a target, return the indices of two *different* elements whose values add up to the target. Exactly one valid answer exists.

## Implementations

| File | Approach | Time complexity | Extra space |
| --- | --- | --- | --- |
| [solution.py](solution.py) | Brute-force search over distinct pairs | O(n²) | O(1) |
| [solution.js](solution.js) | One-pass hash map of previously seen values | O(n) average | O(n) |

### Python — brute force

The nested loops check each pair only once by starting the inner loop after the current index. This keeps the implementation straightforward but scales quadratically with the array size.

### JavaScript — hash map

At each position, calculate the complementary value needed to reach the target. Check whether that complement has already been seen; if so, return both indices. Otherwise, store the current value and index.

Checking **before inserting** prevents the algorithm from matching an element with itself. It also handles duplicates such as `[3, 3]` with target `6`.

## Reflection

The two implementations show a useful progression: starting with a simple exhaustive search and then using a hash map to trade additional memory for faster average lookup.

**Note:** Solution files are preserved from the original attempts, without algorithmic changes.
