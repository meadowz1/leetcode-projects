# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->
My original thought process was to use loops, but later I learned
a solution using a dictionary approach and enumerate(). 

# Approach
I used two for loops and brute forced my way into the solution.

# Complexity
- Time complexity:
It doesn't take long but it could be a lot more efficient in the timing.
Takes around 61ms to complete the testing cases.

# Code
```
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i in range(len(nums) + 1):
            for j in range(i + 1, len(nums)):
                if nums[i] + nums[j] == target:
                    return([i, j])
```
