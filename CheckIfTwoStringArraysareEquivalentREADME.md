# leet-day23

# Word Array Comparison

## Problem Description

Given two string arrays `word1` and `word2`, the task is to determine if the two arrays represent the same string.

A string is represented by an array if the array elements, when concatenated in order, form the string.

## Example

Input:

```
word1 = ["ab", "c"]
word2 = ["a", "bc"]
```

Output:

```
true
```

Explanation:

`word1` represents the string "ab" + "c" -> "abc".

`word2` represents the string "a" + "bc" -> "abc".

Since the strings are the same, the function should return `true`.

## Constraints

- The lengths of `word1` and `word2` are between 1 and 10^3.
- The lengths of each element in both arrays are between 1 and 10^3.
- The sum of lengths of all elements in both arrays is between 1 and 10^3.
- The elements of `word1` and `word2` consist of lowercase letters.

## Approach

To solve this problem, we can concatenate all the elements of both `word1` and `word2` to form two separate strings `str1` and `str2`. Finally, we compare the two strings for equality. If they are the same, the two arrays represent the same string.

## Solution in C++

```cpp
#include <string>
#include <vector>

using namespace std;

class Solution {
public:
    bool arrayStringsAreEqual(vector<string>& word1, vector<string>& word2) {
        string str1, str2;
        for (const string& word : word1) {
            str1 += word;
        }
        for (const string& word : word2) {
            str2 += word;
        }
        return str1 == str2;
    }
};
```

## Complexity Analysis

- Time complexity: O(N), where N is the total number of characters in both `word1` and `word2`.
- Space complexity: O(N), as we need to store the concatenated strings `str1` and `str2`.
