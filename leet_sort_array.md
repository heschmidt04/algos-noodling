# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->
Use a Python built in instead of reinvent the wheel because they have put more thought into making sorted() more efficient. 

It falls under cheap, blue, easy - pick 2 paradigm. 
This can be one of the worst BigO algorithms and folks would probably code around using it for large array sorts. 

# Approach
<!-- Describe your approach to solving the problem. -->
Sorted built in method will always show the array from least to most 
Reference https://www.w3schools.com/python/python_ref_functions.asp 

# Complexity
- Time complexity:
<!-- Add your time complexity here, e.g. $$O(n)$$ -->
As a class it has all the dunders for repr and efficiencies built in 
You can look at the source code with 
import inspect 
**inspect.getsource(sorted)**

- Space complexity:
<!-- Add your space complexity here, e.g. $$O(n)$$ -->
It still is an O(n squared) challenge and folks mentioned the source code for sorted() creates a new list and provide timeit examples
https://stackoverflow.com/questions/4154571/sorted-using-generator-expressions-rather-than-lists/4155652

# Code
```
from typing import List
import inspect

class Solution:
    def sortArray(self, nums: List[int]) -> List[int]:
        return sorted(nums)
        


# Set up the Python instantiated Class 
test = Solution()
# this proves test is an instance of Solution class 
isinstance(test, Solution) 
# Set up the list array of numbers 
nums = [5,2,3,1]
# Use the function inside the class to sort the array of numbers 
test.sortArray(nums)
 
# Show the source code of sorted() Python built-in function 
**inspect.getsource(sorted)**
```
