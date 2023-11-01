# Intuition
You have to take into consideration the math of this problem.
Simply speaking, the program wants to compare each digit with 
one another. Using that knowledge, a little bit of division and
multiplication would make this problem possible without converting
the integers to strings. 

# Approach
I have a value that is stored beforehand for the original X value.
I modify that X value by // it by 10. (To remove a value from the end each time)
I have a seperate Y value, that starts at 0, gets multiplied by 10, and 
gets the remainder of X / 10 added to it each time the loop runs.
The loop this is in runs until the X value reaches or gets lower than 0.
After the loop is complete, the original value is compared to the now flipped Y value. 

# Complexity
- Time complexity:
Without using the String conversion method, this program runs a 52ms runtime with the
test case provided on LeetCode.

# Code
```py
class Solution:
    def isPalindrome(self, x: int) -> bool:
        val = x
        y = 0

        while(x > 0):
            y = y * 10 + (x % 10)
            x = x // 10
        
        if (val < 0):
            return False

        elif (val == y):
            return True

        else:
            return False
        
```
