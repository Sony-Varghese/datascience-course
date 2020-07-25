
# Some Python errors encountered so far in the course.
### a)  Syntax Error
```
>>> print "hi"
  File "<stdin>", line 1
    print "hi"
             ^
SyntaxError: Missing parentheses in call to 'print'. Did you mean print("hi")?
```
In Python 3, builtin print function requires a parentheses,hence above error.

Correct syntax should be,

```
>>> print("hi")
hi
```
### b) Type Error

```
>>> sample_tuple = (3, 5, 10)
>>> sample_tuple[1] = 15
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment
>>>
```
This TypeError happens when an attempted operation on an object is not supported, and is not meant to be. In this case we use tuple which is immutable.

```
>>> sample_set = {1,2,5,7,3}
>>> sample_set[2]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'set' object is not subscriptable
>>>
```
This TypeError is indicating that the function or method is not subscriptable, means they are not indexable like a list. Here we use set,set does not allow you to call using index.

### c) ValueError

```
>>> a = "Hello"
>>> int(a)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: invalid literal for int() with base 10: 'Hello'
>>>
```
Here ValueError means function's(int) argument(a) has an inappropriate type,ie you cannot convert a string to an integer type.

### d) KeyError

```
>>> sample_dict = {'a':"alpha", 1:"first", 2:"second", 3:"third", 4:"fourth"}
>>> sample_dict['b']
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'b'
```
KeyError is raised because the key you are trying to access is not found in the dictionary.

### e) NameError

```
>>> sample_list
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'sample_list' is not defined
>>>
```

NameError is raised when a local or global name is not found. In the above eg sample_list is not defined,hence the error.

### f) IndexError

```
>>> sample_list = [0, 1, "a", "b"]
>>> sample_list[4]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
>>>
```
IndexError is raised because you are trying to access an item at an invalid index.
Above eg has index only up to 3.