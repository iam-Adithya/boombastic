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
# Python Arrays: Prerequisites for LeetCode (Without Inbuilt Functions)

## 1. List Basics (Python's Arrays)
In Python, arrays are implemented as lists. You should know how to:

### Create a List:
```python
arr = []
arr.append(1)
arr.append(2)
arr.append(3)
arr.append(4)
arr.append(5)
```

### Access Elements:
```python
def get_element(arr, index):
    return arr[index]

print(get_element(arr, 0))  # Output: 1
print(get_element(arr, -1)) # Output: 5 (Last element)
```

### Modify Elements:
```python
def update_element(arr, index, value):
    arr[index] = value

update_element(arr, 1, 10)
print(arr)  # Output: [1, 10, 3, 4, 5]
```

### Find Length of a List:
```python
def get_length(arr):
    count = 0
    for _ in arr:
        count += 1
    return count

print(get_length(arr))  # Output: 5
```

## 2. List Slicing (Selecting Subarrays)
### Extract a portion of a list:
```python
def slice_list(arr, start, end):
    result = []
    for i in range(start, end):
        result.append(arr[i])
    return result

print(slice_list(arr, 1, 4))   # Output: [10, 3, 4]
```

## 3. Adding & Removing Elements
### Append (Add to End):
```python
def append_element(arr, value):
    arr += [value]

append_element(arr, 60)
print(arr)  # Output: [1, 10, 3, 4, 5, 60]
```

### Insert (Add at Specific Index):
```python
def insert_element(arr, index, value):
    new_arr = []
    for i in range(get_length(arr)):
        if i == index:
            new_arr.append(value)
        new_arr.append(arr[i])
    arr[:] = new_arr

insert_element(arr, 2, 25)
print(arr)  # Output: [1, 10, 25, 3, 4, 5, 60]
```

### Remove an Element by Value:
```python
def remove_element(arr, value):
    new_arr = []
    for item in arr:
        if item != value:
            new_arr.append(item)
    arr[:] = new_arr

remove_element(arr, 3)
print(arr)  # Output: [1, 10, 25, 4, 5, 60]
```

### Remove Last Element (Pop):
```python
def pop_element(arr):
    new_arr = []
    last = arr[-1]
    for i in range(get_length(arr) - 1):
        new_arr.append(arr[i])
    arr[:] = new_arr
    return last

print(pop_element(arr))  # Output: 60
print(arr)   # Output: [1, 10, 25, 4, 5]
```

## 4. Iterating Through an Array
### Using for Loop:
```python
def print_list(arr):
    for num in arr:
        print(num, end=" ")
    print()

print_list(arr)  # Output: 1 10 25 4 5
```

### Using While Loop:
```python
def print_list_while(arr):
    i = 0
    while i < get_length(arr):
        print(arr[i], end=" ")
        i += 1
    print()

print_list_while(arr)
```

## 5. Searching in an Array
### Check if an Element Exists:
```python
def contains(arr, value):
    for item in arr:
        if item == value:
            return True
    return False

print(contains(arr, 25))  # Output: True
print(contains(arr, 50))  # Output: False
```

### Find Index of an Element:
```python
def find_index(arr, value):
    for i in range(get_length(arr)):
        if arr[i] == value:
            return i
    return -1

print(find_index(arr, 25))  # Output: 2
```

## 6. Sorting an Array
### Sort a List in Ascending Order:
```python
def bubble_sort(arr):
    n = get_length(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

bubble_sort(arr)
print(arr)
```

## 7. Common List Operations
### Find Maximum & Minimum Elements:
```python
def find_max(arr):
    max_value = arr[0]
    for num in arr:
        if num > max_value:
            max_value = num
    return max_value

def find_min(arr):
    min_value = arr[0]
    for num in arr:
        if num < min_value:
            min_value = num
    return min_value

print(find_max(arr))  # Output: 25
print(find_min(arr))  # Output: 1
```

### Sum of All Elements:
```python
def find_sum(arr):
    total = 0
    for num in arr:
        total += num
    return total

print(find_sum(arr))
```

### Count Occurrences of an Element:
```python
def count_occurrences(arr, value):
    count = 0
    for num in arr:
        if num == value:
            count += 1
    return count

print(count_occurrences(arr, 10))  # Output: 1
```


