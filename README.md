# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```Python
''' 
Program for linear search method to match the item in a list
Developed by: Kishore B
RegisterNumber: 23013723
'''
def linearSearch(array,k):
    for i in array:
        if i == k:
            return 1
            break
        else:
            continue
    
array = eval(input())
array.sort()
print(array)
k = eval(input())

result = linearSearch(array,k)
if result == 1:
    print("Element found at index: ",array.index(k))
else:
    print("Element not found")
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```Python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Kishore B
RegisterNumber: 23103723
'''
def BinarySearch(arr, k):
    low=0
    high=len(arr)-1
    mid=0
    while low<=high:
        mid=(high+low)//2
        if arr[mid]<k:
            low=mid+1
        elif arr[mid]>k:
            high=mid-1
        else:
            return mid
    return -1
   
    
    
arr = eval(input())
k = eval(input()) 
arr.sort()
print(arr)
result=BinarySearch(arr,k)
if result != -1:
    print("Element found at index: ",str(result))
else:
    print("Element not found")
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```Python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Kishore B
RegisterNumber: 23013723
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=(high+low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr,k,low,mid-1)
        else:
            return BinarySearch(arr,k,mid+1,high)
    else:
        return -1
    
    
arr = eval(input())
k = eval(input()) 
arr.sort()
print(arr)
result=BinarySearch(arr,k,0,len(arr)-1)
if result != -1:
    print("Element found at index: ",str(result))
else:
    print("Element not found")
```
## Sample Input and Output
#### 1st Program
<img width="658" alt="image" src="https://github.com/Nijeesh-bit/Search-Algorithm/assets/89188014/01289684-a999-4722-b7a8-cc10dacd8b1b">

#### 2nd Program
<img width="594" alt="image" src="https://github.com/Nijeesh-bit/Search-Algorithm/assets/89188014/c1f19f25-8c05-4d92-a5d6-8cf20b3248e4">

#### 3rd Program
<img width="490" alt="image" src="https://github.com/Nijeesh-bit/Search-Algorithm/assets/89188014/45179374-510b-4ee8-8bfb-49e1c07cd961">

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
