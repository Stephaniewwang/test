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

