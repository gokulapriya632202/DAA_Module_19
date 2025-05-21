# EX 1B Merge Sort
## DATE: 07/05/2025
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1. If the array has more than one element, split it into two halves.
2. Recursively apply merge sort on both halves.
3. Compare elements of both halves and merge them into a sorted array.
4. Copy any remaining elements from the left or right half.
5. Return the fully sorted array.  

## Program:
```
/*
Program to implement Merge Sort
Developed by: GOKULA PRIYA P  
Register Number:  212222040044
*/
```

```
def Merge_Sort(S):
    if(len(S)>1):
        mid=len(S)//2
        left=S[:mid]
        right=S[mid:]
        Merge_Sort(left)
        Merge_Sort(right)
        i=j=k=0
        while(i<len(left) and j<len(right)):
            if(left[i]<right[j]):
                S[k]=left[i]
                i+=1
            else:
                S[k]=right[j]
                j+=1
            k+=1
        while(i<len(left)):
            S[k]=left[i]
            i+=1
            k+=1
        while(j<len(right)):
            S[k]=right[j]
            j+=1
            k+=1
    
    
n=int(input())
S=[]
for i in range(n):
    S.append(float(input()))
print("Given array is")
print(*S)
Merge_Sort(S) 
print("Sorted array is")
print(*S)
```

## Output:

![AOA-1B](https://github.com/user-attachments/assets/deb2e14a-2d85-4d88-9fdf-83a6c72ad900)


## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
