def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        # 标记是否发生了交换
        swapped = False
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                # 交换位置
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        # 如果没有发生交换，说明列表已经有序，提前退出
        if not swapped:
            break
    return arr

# 示例
arr = [5, 3, 8, 4, 6]
sorted_arr = bubble_sort(arr)
print(sorted_arr)  # 输出: [3, 4, 5, 6, 8]
#  时间复杂度
最坏情况：O(n²)，当列表是逆序时。

最好情况：O(n)，当列表已经有序时。

平均情况：O(n²)。

4. 空间复杂度
O(1)，因为冒泡排序是原地排序算法，不需要额外的存储空间。

5. 优缺点
优点：

实现简单，代码易于理解。

原地排序，不需要额外的存储空间。

缺点：

效率较低，尤其是对于大规模数据集。

不适合处理几乎已经有序的列表，因为仍然需要进行多次遍历。#
