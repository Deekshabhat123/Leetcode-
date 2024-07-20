**Sliding Window problem **
**Example Input:** `"pwwkew"`

**Steps:**
1. Initialize `l` (left pointer) to 0, `d` (set to keep track of characters in the current substring) to an empty set, and `count` (to store the maximum length) to 0.
2. Iterate through the string with `r` (right pointer):
   - **r = 0, s[r] = 'p'**:
     - 'p' is not in the set, add 'p' to the set.
     - Update `count` to max(0, 0 - 0 + 1) = 1.
   - **r = 1, s[r] = 'w'**:
     - 'w' is not in the set, add 'w' to the set.
     - Update `count` to max(1, 1 - 0 + 1) = 2.
   - **r = 2, s[r] = 'w'**:
     - 'w' is in the set, remove 'p' (s[l]) from the set, increment `l` to 1.
     - 'w' is still in the set, remove 'w' (s[l]) from the set, increment `l` to 2.
     - Add 'w' to the set.
     - Update `count` to max(2, 2 - 2 + 1) = 2.
   - **r = 3, s[r] = 'k'**:
     - 'k' is not in the set, add 'k' to the set.
     - Update `count` to max(2, 3 - 2 + 1) = 2.
   - **r = 4, s[r] = 'e'**:
     - 'e' is not in the set, add 'e' to the set.
     - Update `count` to max(2, 4 - 2 + 1) = 3.
   - **r = 5, s[r] = 'w'**:
     - 'w' is in the set, remove 'w' (s[l]) from the set, increment `l` to 3.
     - Add 'w' to the set.
     - Update `count` to max(3, 5 - 3 + 1) = 3.

**Final Result:** The length of the longest substring without repeating characters is 3, which is `"wke"`.
