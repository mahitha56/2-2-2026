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
