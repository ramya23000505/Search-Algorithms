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
Register Number: 212223230169
Developed by: RAMYA R
i)	#Use a linear search method to match the item in a list.
```
def search(array,key,n):
    for i in range(0,n):
        if key==array[i]:
            return i
    return -1
array=eval(input())
key=int(input())
array.sort()
n=len(array)
print(array)
result=search(array,key,n)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binary(array,key,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            low=mid+1
        elif array[mid]>key:
            high=mid-1
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:    
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def binary(array,key,low,high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            return binary(array,key,mid+1,high)
        elif array[mid]>key:
            return binary(array,key,low,mid-1)
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:    
    print("Element found at index: ",result)
```
## Sample Input and Output
#Use a linear search method to match the item in a list.
![Screenshot 2024-03-27 091442](https://github.com/ramya23000505/Search-Algorithms/assets/149370791/3800a9de-0cec-4828-83cd-7a561832de35)
![Screenshot 2024-03-27 091449](https://github.com/ramya23000505/Search-Algorithms/assets/149370791/41ab0a8c-0462-4b50-bf1f-029dcdd006c6)
# Find the element in a list using Binary Search(Iterative Method).
![Screenshot 2024-03-27 091530](https://github.com/ramya23000505/Search-Algorithms/assets/149370791/637ead3c-157a-44e3-bd73-4ac8c72e126b)
![Screenshot 2024-03-27 091537](https://github.com/ramya23000505/Search-Algorithms/assets/149370791/d045e78a-f190-4d0b-97a7-48ae83020713)
# Find the element in a list using Binary Search (recursive Method).
![Screenshot 2024-03-27 091608](https://github.com/ramya23000505/Search-Algorithms/assets/149370791/c2d7aee9-dba1-473c-a2af-86c431adb9c0)
![Screenshot 2024-03-27 091616](https://github.com/ramya23000505/Search-Algorithms/assets/149370791/3ca93c26-4a9d-4653-97f9-0a97f0cca386)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
