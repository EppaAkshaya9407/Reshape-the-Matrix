# Reshape-the-Matrix
class Solution:
    def matrixReshape(self, mat: List[List[int]], r: int, c: int) -> List[List[int]]:
        n=len(mat)
        m=len(mat[0])
        if n*m!=r*c:
            return mat
        a=[]
        for i in range(n):
            for j in range(m):
                 a.append(mat[i][j])
        res=[]
        k=0
        for i in range(r):
            r1=[]
            for j in range(c):
                r1.append(a[k])
                k+=1
            res.append(r1)
        return res
