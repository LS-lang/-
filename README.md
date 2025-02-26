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
