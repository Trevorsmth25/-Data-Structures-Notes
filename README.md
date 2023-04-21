# -Data-Structures-Notes

Notes about Data structure The matrix. In computer science and python 3 we start a data structure that has values in rows and columns. It's like a table of values which utilizes a list within a list.A matrix is a two-dimensional array of numbers. In Python, matrices can be represented using nested lists, where each sublist represents a row of the matrix. For example, the following matrix: A = {1234} {5678} Two arrays of data a list in a list^ this is a mathmaticcal matrix Diagram We let A repersent the matrix. Matrix A can have m rows and n colums in the case above 4 colums 2 rows.
In python 3 there is no data structure called "Matrix". Therefore thats why we have to code a list within a list to create the matrix while following the same rules of a regular matrix. These rules include all rows and colums must have the same number of values All items in the 2d list must be of the same data type Since indexing always starts at 0 ... row 1 is technically located at matrix_A[0]
#List Comprehension in Python 3 Is a concise method in python 3. This technique is commonly used when the list is a member of another list/sequence/iterable data that fits a condition. It can also be used when the list is a result of some operation applied to it's items. The function lambda would be used in these cases. It consists of brackets containing an expression followed by a for clause, then zero or more for or if clauses. The expression is evaluated once for each item in the sequence resulting in a new list. For example, the following list comprehension creates a list containing the squares of all the numbers from 1 to 10. An example of list comprehension is to create a code that squares all number 0-10
Old Method
squares = [] for i in range(10): squares.append(i ** 2)
print('Our result: %s' % squares) Our result: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81] New
List Comprehension
squares = [i**2 for i in range(10)]
print('Our new result: %s' % squares) how does it work It works by consisting a square bracet, one or more clauses to explain i's members, then a zero or more If causes depending on the complexity of the code
Map and Filter in python 3
The map and filter function are both built in python functions. The idea of the Map function is to apply a function to an iterable data. Formatting: map(function_name, sequence)
-- function_name: any function (built-in or selfmade) that returns a desired value of choice -- sequence: any iterable data type
Example
Example
def square(num): ''' squares the given num argument ''' return num ** 2
end of square
array = list(range(1,11)) square_array = list(map(square, array))
print('Original Array:', array) print('Array Squared:', square_array) Original Array: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] Array Squared: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100] One thing to note about the map function is that it dosent return a specific data type but rather python iterable data. Therefore after using the map function we have to excute a list function on it
Filter Function
The idea of the filter function is to filter out items from a data set that meets a certain condition.
Formatting: filter(bool_returning_function, sequence)
-- function: The function name we provide for filter() must be return a boolean value ... should also be able handle the items inside the sequence as its arguments -- sequence: any iterable data type Filter is a function that filters the given iterable with the help of a function that tests each element in the iterable to be true or false Example3:
def isOdd(x): ''' isOdd() returns True if x is odd.''' return x % 2 != 0
array = list(range(1,101)) odds = list(filter(isOdd, array))
print('Odd Numbers from 1 to 100:', odds) Odd Numbers from 1 to 100: [1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51, 53, 55, 57, 59, 61, 63, 65, 67, 69, 71, 73, 75, 77, 79, 81, 83, 85, 87, 89, 91, 93, 95, 97, 99] It is true that this can be done differently, but this was a simplistic use of filter to show we can filter out variables that satisfies condition… aka the condition is True.
#Tuples in python 3 Tuples are a sequence of immutable python objects. These sequences are like lists and strings with key diffrences It must allow different datatypes as items, must be iterable,it must be nestable whixh is like a list within a list.
How to use tuples
Tuples are declared with parenthesis … aka round brackets () is an empty tuple (50,) is a singleton tuple; the comma is required Tuples are sliceable; therefore, indexable using square brackets A singleton is an iterable data structure with only single item.
Example: Tuple Example 1 tup = ('C', ' Java', 'Python') empty_tup = () single_tup = ('Park',)
print(tup) print(empty_tup) print(single_tup) ('C', ' Java', 'Python') () ('Park',) Tuple O
Tuples are iterable, indexable, and slicable. Tuple Packing and unpacking. Explanation: Packing collect multiple variable’s values and assign it to a single variable Unpacking help us assign certain values from a tuple to different variables This becomes very useful skill when combined with variable arguments for Function Definition and Function Calls
Sets
Sets are a data type in python 3 that repersents am unordered grouping of distinct objects. With no duplicated elements. They are typically used to store and handle data, like a collection of singular items or a set of singular values. A set can not have duplicate elements and each element must be hashable by definition. Sets can be used by using the curly bracet or the built in set function. To define a set example:
Set definition examples:
example_set1 = {1, 2, 3} example_set2 = {'h','e','l','l','o'}
print('example_set1:', example_set1) print('example_set2:', example_set2) # Notice there is only 1 'l'; Also notice the order of the values outputted print('--')
singleton_set = {7} empty_set = set() # this is because {} is reversed for a different feature in python 3.
print('Singleton:', singleton_set) print('Empty Set:', empty_set)
One key operations with sets is membership:
A set has no duplicates -A set’s membership operation is one of the fastest operations compared to strings, lists, or tuples this will be covered more when we look at the concept of: complexity -By using membership operator, we can be certain a target exists or does not exist in our data Example of membership: example_set = set('hello')
print("Membership of: 'h'", 'h' in example_set) print("Non-Membership of: 'z'", 'z' not in example_set) membership of h is = True Non-membership of z: True Because there is no ordure of sets there is no concept of indexing or slicing with a set but they are iterable ##Dictionary in python 3: Dictionary is a data type that stores a collection of (key,value) pairs, such that each possible key appears at most once in the collection Common Operations: -Adding a Pair -Removing a pair -modifying an existing pair -lookup of a value associated with a key
Python 3 Sets are mutable: Adding and Removing Values
Sets are mutable; therefore, we can add and remove values There are also methods much lists that can affect the original sets as well
#Powering Up sets: Sets can use vast operators to help us do complex calculations. Most of these operators will have a method counterpart because sets are mutable Our operators: Union Intersection Difference Symmetric Difference Proper Subset Subset Proper Superset Superset
When two sets do not share a common value they are considered disjointed sets support Comprehension Sets aren’t sliceable nor indexable Sets cannot have sets inside them Sets do not have order; nor order of insertion Sets cannot guarantee that their values will be in order Sets do not record a value’s position
#Defining Dictionary Like sets dictionary use {} but there item format is diffrent with each item in a dictionary be a pair of key: Value Dictionary example:
Dictionary Example
sammy = { 'username': 'sammy', 'online': True, 'followers': 42 }
Dictionary properties: each item in dictionary is a key or value pair KEYS: keys are a unique address for dictionary values loctions they must be immutable unique therfore two keys cannot values exist in a single dictionary the newest created item with a duplicate KEY superceeds the previouse declaration
Values: Vaues of a dictionary within a key can be any data type Dictionary can modify existing values by referencing the key. We can add new values to dictionary by creating a new key. We can overwrite a value at an existing key by refrencing and recreating the value for it. We can also use deletions in dictionary we can empty the dictionary or delete the key, we can even delte the dictionar. We can use membership in dicctionary using in and not in operators to check if key exists.
There are built-in functions interations with dictionaries
Dictionary methods: Let A and B be a dictionary
A.keys() –> Returns a sequence of keys/addresses in A A.values() –> Returns a sequence of item values in A A.items() –> Returns a sequence of key,item pairs in A A.get(address) –> Returns the item value at address A.update(B) –> Extends A with the dictionary of key,value pairs of B
Dictionaries are iterable
