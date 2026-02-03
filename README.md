# 605. Can Place Flowers (Easy)

## Problem Description
You have a long flowerbed where some plots are planted (1) and some are empty (0). Flowers cannot be planted in adjacent plots. Given an array `flowerbed` and an integer `n`, return `true` if `n` new flowers can be planted without violating the rule.

### Example
- **Input:** flowerbed = [1,0,0,0,1], n = 1
- **Output:** true

## Approach: Greedy Strategy
The optimal way to solve this is to iterate through the array and plant a flower at the **first available valid spot**.

### Logic:
1. Traverse the `flowerbed` array.
2. For each plot, check if it's empty (`0`).
3. Check neighbors:
   - If it's the first element, check only the right neighbor.
   - If it's the last element, check only the left neighbor.
   - Otherwise, check both.
4. If valid, "plant" the flower by setting the value to `1` and decrementing `n`.
5. If `n` reaches 0, return `true`.

## Complexity Analysis
- **Time Complexity:** $O(N)$ - We traverse the array once.
- **Space Complexity:** $O(1)$ - We modify the input array in place without extra data structures.
