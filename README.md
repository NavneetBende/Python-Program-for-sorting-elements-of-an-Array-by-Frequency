Sorting elements of an Array by Frequency in Python
Here, in this article we will discuss the program for sorting elements of an array by frequency in python programming language. We will discuss various algorithms for sorting.

Python Program for sorting elements of an Array by Frequency
Here, we will discuss the following methods in this page.

Method 1 : Using Collections.counter()
Method 2 : Using Iterables.
Method 3 : Using sorted() inbuilt function.
Let’s discuss above three methods one by one,

Method 1 :
In this method we will use Collections.counter() to count the occurrence of element present in the list.

Collections counter()
Python Counter is a container that will hold the count of each of the elements present in the container.
The counter is a sub-class available inside the dictionary class.
Using the Python Counter tool, you can count the key-value pairs in an object, also called a hash table object
Method 1 : Code in Python
Run
from collections import Counter
ini_list = [10, 20, 30, 40, 40, 50, 50, 50]

# sorting on bais of frequency of elements
result = [item for items, c in Counter(ini_list).most_common() for item in [items] * c]

# printing final result
print(str(result))
Output
[50, 50, 50, 40, 40, 10, 20, 30]
Related Pages
Sort the elements of an array

Finding the frequency of elements in an array

Finding the Longest Palindrome in an Array

Counting Distinct Elements in an Array

Finding  Repeating elements in an Array

Method 2 :
In this method we will use iterables for sorting on the basis of frequency of elements.

Iterables in Python
Iterable is an object which can be looped over or iterated over with the help of a for loop.
Objects like lists, tuples, sets, dictionaries, strings, etc. are called iterables.
In short and simpler terms, iterable is anything that you can loop over.
Method 2 : Code in Python
Run
from collections import Counter
from itertools import repeat, chain
ini_list = [10, 20, 30, 40, 40, 50, 50, 50]

# sorting on bais of frequency of elements
result = list(chain.from_iterable(repeat(i, c) for i, c in Counter(ini_list).most_common()))

# printing final result
print(str(result))
Output
[50, 50, 50, 40, 40, 10, 20, 30]
Method 3 :
In this method we will use sorted() inbuilt function.

sorted() function in Python
Python sorted() function returns a sorted list from the iterable object.
Sorted() sorts any sequence (list, tuple) and always returns a list with the elements in a sorted manner, without modifying the original sequence.
Key(optional) : A function that would server as a key or a basis of sort comparison.
Method 3 : Code in Python
Run
from collections import Counter
from itertools import repeat, chain
ini_list = [10, 20, 30, 40, 40, 50, 50, 50]

# sorting on bais of frequency of elements
result = sorted(ini_list, key = ini_list.count, reverse = True)

# printing final result
print(str(result))
Output
[50, 50, 50, 40, 40, 10, 20, 30]
