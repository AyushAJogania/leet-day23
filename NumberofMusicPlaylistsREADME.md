# leet-day23

# Music Player Playlist Combinations

## Problem Description

You have a music player containing `n` different songs. During your trip, you want to listen to `goal` songs (not necessarily different) and to avoid boredom, you will create a playlist with the following rules:

1. Every song is played at least once.
2. A song can only be played again if `k` other songs have been played.

Given the number of songs `n`, the number of songs you want to listen to `goal`, and the value of `k`, you need to find the number of possible playlists that you can create. Since the answer can be very large, return it modulo 10^9 + 7.

## Example

### Input

```
n = 3, goal = 3, k = 1
```

### Output

```
6
```

### Explanation

There are 6 possible playlists: [1, 2, 3], [1, 3, 2], [2, 1, 3], [2, 3, 1], [3, 1, 2], and [3, 2, 1].

## Constraints

- 0 <= k < n <= goal <= 100

## Approach and Complexity

To solve this problem, we can use dynamic programming to compute the number of ways to create the playlists of length `i` using `j` distinct songs. We will use a 1D array to store the dynamic programming results to optimize space complexity.

- Time complexity: O(goal * n)
- Space complexity: O(n)


This solution provides an optimized approach to find the number of possible playlists that meet the given criteria.
