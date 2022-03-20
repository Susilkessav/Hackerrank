# Question
In this HackerRank Arrays - DS problem, we need to write a program that can take an integer array as input and then reverse it. also, we need to make a reveseArray function that can return the reverse array. For example if we give input  arr = [2,3,5] then it must return [5,3,2].

# CODE 
## Python 

```py
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'reverseArray' function below.
#
# The function is expected to return an INTEGER_ARRAY.
# The function accepts INTEGER_ARRAY a as parameter.
#

def reverseArray(a):
    a = a[::-1]
    b = []
    for i in range(len(a)):
        b.append(a[i])
    return b
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    arr_count = int(input().strip())

    arr = list(map(int, input().rstrip().split()))

    res = reverseArray(arr)

    fptr.write(' '.join(map(str, res)))
    fptr.write('\n')

    fptr.close()
```
In reverseArray function. When you do a[::-1], it starts from the end towards the first taking each element. So it reverses a. This is applicable for lists/tuples as well. And in the for loop we appending the a elements in the reverse order so we can return the list.
