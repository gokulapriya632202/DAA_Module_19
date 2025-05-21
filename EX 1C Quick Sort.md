# EX 1C Quick Sort
## DATE: 07/05/2025
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm
1. Select a pivot element from the array (commonly the first or last element).
2. Partition the array into two subarrays: elements less than pivot and elements greater than or equal to pivot.
3. Place the pivot between the two subarrays at its correct position.
4. Recursively apply Quick Sort to the left subarray.
5. Recursively apply Quick Sort to the right subarray.

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: GOKULA PRIYA P
Register Number:  212222040044
*/
```

```
def quick_sort(alist,start,end):
    if end-start>1:
        p=partition(alist,start,end)
        quick_sort(alist,start,p)
        quick_sort(alist,p+1,end)
def partition(alist,start,end):
    pivot=alist[start]
    i=start+1
    j=end-1
    print("pivot: ",pivot)
    while True:
        while(i<=j and alist[i]<=pivot):
            i=i+1
        while(i<=j and alist[j]>=pivot):
            j=j-1
        if i<=j:
            alist[i],alist[j]=alist[j],alist[i]
        else:
            alist[start],alist[j]=alist[j],alist[start]
            return j
            
            
alist=[]
n=int(input())
for i in range(n):
    alist.append(int(input()))
print("Input List\n",alist)


quick_sort(alist,0,len(alist))
print('Sorted List\n',alist)
```
## Output:
![Uploading AOA-1C.png…]()



## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
