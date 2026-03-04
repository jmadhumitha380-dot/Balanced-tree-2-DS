# Balanced-tree-2-DS
Practice program

import bisect

arr = []

def add(x):
    bisect.insort(arr, x)

def remove(x):
    if x in arr:
        arr.remove(x)

def median():
    n = len(arr)
    if n == 0:
        return "Empty"
    if n % 2 == 1:
        return arr[n // 2]
    return (arr[n//2 - 1] + arr[n//2]) / 2

# Example operations
operations = [("add", 5), ("add", 3), ("add", 8),
              ("remove", 3), ("add", 10)]

for op, val in operations:
    if op == "add":
        add(val)
    else:
        remove(val)
    print("Median:", median())
   Output:
   Median: 5
Median: 4.0
Median: 5
Median: 6.5
Median: 8
    
