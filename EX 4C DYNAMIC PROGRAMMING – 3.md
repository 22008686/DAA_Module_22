# EX 4C DYNAMIC PROGRAMMING – 3
## DATE:05.04.2025
## AIM:
Given a sequence, find the length of the longest palindromic subsequence in it.

## Algorithm:
1. Initialization
2. DP Transition
3. Final Result

## Program:
```

Program to implement to find the length of the longest palindromic subsequence in it

.
Developed by: M.PAVITHRA
Register Number:212222100032
def Lps(X):
    n=len(X)
    dp=[[0 for _ in range(n)] for _ in range(n)]
    
    for x in range(n):
        dp[x][x]=1
        
    for l in range(2,n+1):
        for i in range(n-l+1):
            j=i+l-1
            if X[i]==X[j]:
                dp[i][j]=dp[i+1][j-1]+2
            else:
                dp[i][j]=max(dp[i+1][j],dp[i][j-1])
    return dp[0][n-1]
    
X=input()
print("The length of the LPS is",Lps(X))
        

```

## Output:

![Screenshot 2025-04-30 205608](https://github.com/user-attachments/assets/eaa89930-6956-456e-a912-724cef55adf5)


## Result:
Thus the program was executed successfully for finding the length of longest palindromic string.
