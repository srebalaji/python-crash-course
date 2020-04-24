# Python crash course

This course is for people who already have experience in programming and want to learn Python quickly without wasting much time in finding the right course.

This course is created out of frustration of not finding any course online or any other resource to learn Python for programmers from other language background. 

In this course, I will be covering all the basics of Python (in-depth lessons will be added later on) so that you can get started in the language very quickly.


- [Setting up the environment](https://github.com/srebalaji/python-crash-course-for-non-python-programmers#setting-up-the-environment)
- [Hello World](https://github.com/srebalaji/python-crash-course-for-non-python-programmers#hello-world)


## Setting up the environment
You can consider installing Python 3. I recommend using vs-code to code. It has lots of extensions to configure so that you can setup your environment in just few minutes.

## Hello world
```
print("Hello world")
```

I think pretty sure how to run this program :P. Save the program with `.py` extension. And run `python hello.py` or `python3 hello.py`

In this whole tutorial, we will follow `python3`. `python2` will be discontinued by 2020. So I think it’s good to go with latest version.


## Variables and data types
Variables can contain in letters, numbers and in underscores. 

### Strings

```python
# This is comment in Python
msg_from_computer = "Hello" # String
another_msg ='Hello in single quote' # This is also a String.

print(msg_from_computer + " World..!")

# Type will return the data type.
print(type(msg_from_computer)) # <type 'str'>. We will see the explanation of this later.
```

### Numbers

```python
2
2 * 3
2 ** 7
(2 + 3) * 4
```

### Float

```python
2.7

0.1 + 0.2 # 0.3
2 * 0.1 # 0.2
```

Careful in Concatenation

```python
count = 5

print("I need" + count + "chocolates") # This line will throw error. As count is a integer, you have to type cast it.

print("I need" + str(count) + "chocolates") # This will work
```

### Bool

```python
True # First letter is caps

False

bool("some value") # Returns True

bool("") # Returns False

bool(1) # Returns True

```

### List

List are basically like array. In Python world, they call it as `List`. And they are ordered. 

```python
numbers = ["one", "two", "three"]

numbers[0] # one

numbers[-1] # three. This is awesome. If we pass negative value Python will start from the end.

numbers[-2] # two

len(numbers) # 3. It just returns the length

numbers.append("four") # Append will add the element to the last. ["one", "two", "three", "four"]

numbers.insert(1, "wrong_one") # Insert will insert the particular value to the appropiate position. ["one", "wrong_one", "two", "three", "four"]

# Deleting a value is somewhat weird
del numbers[1] # Will delete the value in the appropiate position. "one", "two", "three", "four"]

# Pop will help you to remove the last element of an array
popped_element = numbers.pop()

print(popped_element) # four
print(numbers) # ["one", "two", "three"]

# Remove elements by value
numbers.remove("two") # ["one", "three"]. This will remove only the first occurence of an array.

# Sorting
alpha = ["z", "c", "a"]
alpha.sort()
print(alpha) # ["a", "c", "z"] Sorting is permanent. now `alpha` is sorted permanently

alpha.sort(reverse=True)
print(alpha) #["z", "c" , "a"] Reverse sorting.

alpha = ["z", "c", "a"]
print(sorted(alpha)) # ["a", "c", "z"] This will just return the sorted array. It wont save the sorted array to the variable itself.

print(alpha) # ["z", "c", "a"] As you can see, it's not sorted

# Reversing an array
nums = [10, 1, 5]
nums.reverse()
print(nums) # [5, 1, 10] It just reverses an array. It means it reads from last. It's not sorting it. It's just changing the chronological order.

# Slicing elements
alpha = ['a', 'b', 'c', 'd', 'e']
alpha[1:3] # ['b', 'c']. The first element is the starting index. And Python stops in the item before the second index.
alpha[2:5] # ['c', 'd', 'e']

alpha[:4] # [ 'a', 'b', 'c', 'd'] In this case, the first index is not present, so Python startes from the beginning.

alpha[:3] # ['a', 'b', 'c']

alpha[3:] # ['d', 'e'] In this case, last index is not present. So it travels till the end of the list.

alpha[:] # ['a', 'b', 'c', 'd', 'e'] There is no starting or ending index. So you know what happens. And this helps you in copying the entire array. I think I don't have to explain that if you copy the array, then any changes in the original array won't affect the copied array.

another_alpha = alpha # This is not copying the array. Any changes in alpha will affect another_alpha too. 
```

### Tuple
Tuples are just like lists but they are **immutable** So you can’t add or update in tuples. You can just read elements. And remember like lists, Tuple is also sequential.

```python
nums = (1, 2, 3)

print(nums) # (1, 2, 3)

print(nums[0]) # 1

print(len(nums)) # 3

empty_tuple = () # empty tuple. Length is zero.

num = (1, ) # Note the trailing comma. When defining a single element in the tuple, consider adding a trailing comma.

num = (1)
print(type(num)) # <type 'int'> It won't return a tuple. Because there is no trailing comma.

# Creating a new tuple from the existing tuple
nums = (1, 2, 3)
char = ('a', )
new_tuple = nums + char
print(new_tuple) # (1, 2, 3, 'a')
```

### Sets
Sets are unordered collections with no duplicate elements.

```python
alpha = {'a', 'b', 'c', 'a'}

print(alpha) # set(['a', 'c', 'b']) As you can see, duplicates are removed in sets. And also the output is not ordered.

# Accessing items in set
# You can't access by index because Sets are unordered. You can access it only by loop. Don't worry about the for loop, we will get that in-depth in the following section.
for ele in alpha:
	print(ele)

# To add element into the set
alpha.add('s')

# add can be used to insert only one element. If you want multiple elements, then update will be handy
alpha.update(['a', 'x', 'z']) # set(['a', 'c', 'b', 'x', 'z']) Remember duplicated are removed.

# Length of the alpha
len(alpha) # 5

# Remove the element from the set
alpha.remove('a')
alpha.discard('a') # It's safer to use discard than remove. Discard will never throw an error even if the element is not present in the set but remove will do.



```
