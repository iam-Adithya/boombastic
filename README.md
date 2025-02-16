# boombastic
# Python Arrays: Prerequisites for LeetCode

## 1. List Basics (Python's Arrays)
In Python, arrays are implemented as lists. You should know how to:

### Create a List:
```python
arr = [1, 2, 3, 4, 5]
```

### Access Elements:
```python
print(arr[0])  # Output: 1
print(arr[-1]) # Output: 5 (Last element)
```

### Modify Elements:
```python
arr[1] = 10
print(arr)  # Output: [1, 10, 3, 4, 5]
```

### Find Length of a List:
```python
print(len(arr))  # Output: 5
```

## 2. List Slicing (Selecting Subarrays)
### Extract a portion of a list:
```python
arr = [10, 20, 30, 40, 50]
print(arr[1:4])   # Output: [20, 30, 40]
print(arr[:3])    # Output: [10, 20, 30] (First 3 elements)
print(arr[-3:])   # Output: [30, 40, 50] (Last 3 elements)
print(arr[::-1])  # Output: [50, 40, 30, 20, 10] (Reversed)
```

## 3. Adding & Removing Elements
### Append (Add to End):
```python
arr.append(60)
print(arr)  # Output: [10, 20, 30, 40, 50, 60]
```

### Insert (Add at Specific Index):
```python
arr.insert(2, 25)
print(arr)  # Output: [10, 20, 25, 30, 40, 50]
```

### Remove an Element by Value:
```python
arr.remove(30)
print(arr)  # Output: [10, 20, 40, 50]
```

### Remove Last Element (Pop):
```python
last = arr.pop()
print(last)  # Output: 50
print(arr)   # Output: [10, 20, 40]
```

### Delete an Element by Index:
```python
del arr[1]
print(arr)  # Output: [10, 40]
```

## 4. Iterating Through an Array
### Using for Loop:
```python
arr = [1, 2, 3, 4, 5]
for num in arr:
    print(num, end=" ")  # Output: 1 2 3 4 5
```

### Using enumerate() to Get Index & Value:
```python
for i, num in enumerate(arr):
    print(f"Index {i}: {num}")
```

### Using While Loop:
```python
i = 0
while i < len(arr):
    print(arr[i], end=" ")
    i += 1
```

## 5. Searching in an Array
### Check if an Element Exists:
```python
arr = [10, 20, 30, 40]
print(30 in arr)  # Output: True
print(50 in arr)  # Output: False
```

### Find Index of an Element:
```python
print(arr.index(30))  # Output: 2
```

## 6. Sorting an Array
### Sort a List in Ascending Order:
```python
arr = [50, 10, 30, 20, 40]
arr.sort()
print(arr)  # Output: [10, 20, 30, 40, 50]
```

### Sort in Descending Order:
```python
arr.sort(reverse=True)
print(arr)  # Output: [50, 40, 30, 20, 10]
```

### Sort Without Modifying the Original List:
```python
arr = [50, 10, 30, 20, 40]
sorted_arr = sorted(arr)
print(sorted_arr)  # Output: [10, 20, 30, 40, 50]
print(arr)  # Original list remains unchanged
```

## 7. Common List Operations
### Find Maximum & Minimum Elements:
```python
arr = [10, 20, 30, 40, 50]
print(max(arr))  # Output: 50
print(min(arr))  # Output: 10
```

### Sum of All Elements:
```python
print(sum(arr))  # Output: 150
```

### Count Occurrences of an Element:
```python
arr = [10, 20, 30, 20, 40, 20]
print(arr.count(20))  # Output: 3
```

## 8. List Comprehension (One-Line Loops)
### Create a List from a Range:
```python
arr = [x for x in range(1, 11)]
print(arr)  # Output: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

### Filter Even Numbers:
```python
arr = [x for x in range(1, 11) if x % 2 == 0]
print(arr)  # Output: [2, 4, 6, 8, 10]
```

### Square All Numbers in a List:
```python
arr = [x**2 for x in range(1, 6)]
print(arr)  # Output: [1, 4, 9, 16, 25]
```

