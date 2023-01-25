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
```python
''' 
Program for linear search method to match the item in a list
Developed by: Shaik Sameer Basha
RegisterNumber: 22004926
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1

array = eval(input())
k=eval(input())
n=len(array)
array.sort()
result=linearSearch(array,n,k)
if(result==-1):
    print(array)
    print('Element not found')
else:
    print(array)
    print("Element found at index: ",result)


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```python
''' 
Program for linear search method to match the item in a list
Developed by: Shaik Sameer Basha
RegisterNumber: 22004926
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1

array = eval(input())
k=eval(input())
n=len(array)
array.sort()
result=linearSearch(array,n,k)
if(result==-1):
    print(array)
    print('Element not found')
else:
    print(array)
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: shaik sameer basha
RegisterNumber: 22004926
'''
def binarysearch(arr,k,low,high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return binarysearch(arr,k,low,mid-1)
        else:
            return binarysearch(arr,k,mid+1,high)
    else:
        return -1
arr=eval(input())
arr.sort()
k=eval(input())
result=binarysearch(arr,k,0,len(arr)-1)
if (result==-1):
    print (arr)
    print("Element not found")
else:
    print (arr)
    print("Element found at index: ",result)





```
## Sample Input and Output



![linearsearch_output](https://user-images.githubusercontent.com/118707756/214650536-ee3cf9b0-3e3c-4829-8c01-fe4c59195c37.png)


![iterative_output](https://user-images.githubusercontent.com/118707756/214650675-4ee07e41-b7b0-4d4b-8adb-e540706ed4c4.png)



![recursive_output](https://user-images.githubusercontent.com/118707756/214650753-52af7465-97f6-40a5-8283-b5e9a217941c.png)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.
