class Solution:
    def isMatch(self, string: str, pattern: str) -> bool:
        n = len(pattern)
        m = len(string)
        dp = [[False for j in range(m+1)]for i in range(n+1)]
        dp[0][0] = True
        for i in range(1,m+1):
        
            dp[0][i] = 0
        for i in range(1,n+1):
        
            a = True
            for j in range(0,i):
            
                if pattern[j]!='*':
                
                    a = False
                
            dp[i][0] = a
            
        for i in range(1,n+1):
            for j in range(1,m+1):
                if pattern[i-1] == string[j-1] or pattern[i-1] == '?':
                    dp[i][j] = dp[i-1][j-1]
                elif pattern[i-1] == '*':
                    dp[i][j] = dp[i-1][j] or dp[i][j-1]
                else:
                    dp[i][j] = False
        return dp[n][m]
