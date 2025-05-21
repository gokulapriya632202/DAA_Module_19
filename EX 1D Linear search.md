# EX 1D Linear search
## DATE: 07/05/2025
## AIM:
To write a python program for a search function with parameter list name and the value to be searched using string values.



## Algorithm
1. Loop through each element in the tuple.
2. Compare the current element with the target value x.
3. If the element matches x, print that the element was found and stop the search.
4. If no match is found after checking all elements, print that the element was not found.
5. End the function. 

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: GOKULA PRIYA P
Register Number:  212222040044
*/
```

```
def search(Tuple,x):
    for i in range(len(Tuple)):
        if(Tuple[i]==x):
            return 1
    return 0
n=int(input())
arr=[]
for i in range(n):
    arr.append(float(input()))
Tuple=tuple(arr)
x=float(input())
result=search(Tuple,x)
if(result==1):
    print(x,"Found")
else:
    print(x, "Not Found")

```

## Output:
![AOA-1D](https://github.com/user-attachments/assets/c46aeb58-63df-46d8-8414-3fa3f30acb9c)



## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
