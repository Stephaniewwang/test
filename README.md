#插入排序，算法学习的开始，加油！
# cha ru pai xu
A = [3, 4, 11, 5, 0, 4, 7, 2, 4]
for i in range(1,len(A)):
    j = i-1
    key = A[i]
    while j>=0 and A[j] > key:  ＃倒序改为A[j]<key
        A[j+1] = A[j]
        j = j-1
    A[j+1] = key
print A
＃从A的第二个元素开始插入排序，与前面的元素依次比较大小，相当于每比较一次数组元素个数加一，整体右移一个位置，较大的往后排，较小的往前排


#分治排序，重点在于将问题分解为几个部分分别排序，最后再汇总
# fen zhi pai xu
A = [2, 3, 45, 3, 5, "inf"] #inf为无穷，相当于一个标记
B = [2, 5, 9, 21, 4, 23, "inf"]
for i in range(1,len(A)):
    j = i-1
    key = A[i]
    while j >= 0 and A[j] > key:
        A[j+1] = A[j]
        j = j-1
    A[j+1] = key
    
for i in range(1,len(B)):
    j = i-1
    key = B[i]
    while j>=0 and B[j] > key:
        B[j+1] = B[j]
        j = j-1
    B[j+1] = key

print A,B
C = []
a=0
b=0
for i in range(0,len(A+B)-2):
    if A[a] > B[b]:
        C.append(B[b]) # 注意Python中list相当于数组，数组增加元素的方法为X.appednd(x)
        b = b+1
    else:
        C.append(A[a])
        a = a+1
print C

