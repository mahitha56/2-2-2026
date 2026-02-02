# 2-2-2026
i can use split function because words wise i want to return 
thats why i am using these
problem
class Solution:
    def countSegments(self, s: str) -> int:
        s1=s.split()
        return len(s1)
        
#prblm
class Solution:
    def canConstruct(self, ransomNote: str, magazine: str) -> bool:
        count=Counter(magazine)
        for i in ransomNote:
            if count[i]==0:
                return False
            count[i]-=1
        return True
#
return n*(n+1)//2 - sum(nums)
Let’s understand it very clearly step-by-step.
🎯 Problem
You have numbers from:

0 to n
But one number is missing.
Example:
nums = [3, 0, 1]
Range should be:

0, 1, 2, 3
Missing = 2

🔹 Step 1 — Sum formula
We use math formula:

Sum of first n numbers:
𝑛
(
𝑛
+
1
)
/
2
n(n+1)/2
In Python:

n*(n+1)//2
Why?

Because:

0+1+2+3 = 6
Formula:

3*4/2 = 6
🔹 Step 2 — Find actual sum
sum(nums)
Example:

sum([3,0,1]) = 4
🔹 Step 3 — Subtract
expected sum - actual sum
6 - 4 = 2
👉 Missing number

✅ Full working code
def missingNumber(nums):
    n = len(nums)
    return n*(n+1)//2 - sum(nums)
🔹 Why // instead of / ?
/  → float
// → integer
We want integer.

Example:

10/2  = 5.0 ❌
10//2 = 5   ✅
🔹 Dry run visually
nums = [0,1,3]
n = 3

expected = 3*4//2 = 6
actual   = 0+1+3 = 4

6 - 4 = 2
Answer = 2

🔥 Complexity
Time  = O(n)
Space = O(1)
Best possible ✅

🧠 Easy memory trick
Think:

👉 "Full sum − present sum = missing"

#prb
class Solution:
    def missingNumber(self, nums: List[int]) -> int:
        #return nums*(nums+1)//2-sum(nums)
        n=len(nums)  
        return n*(n+1)//2 - sum(nums)
