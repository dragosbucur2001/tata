# What are classes/types?

Every variable has a value and a type associated with it.

```python
foo = 5
```

The variable "foo" currently has a value of 5. In order to find out the
type of variable "foo" you can use the function type() (e.g. type(foo))

```python
foo = 5
print(type(foo)) # will print: <class 'int'>

bar = "Hello"
print(type(bar)) # will print: <class 'str'>

baz = [1, 2]
print(type(baz)) # will print: <class 'list'>
```

In the above example:

* `<class 'int'>` - means that the variable is of type integer, it holds
an integer value
* `<class 'str'>` - variable is of type string
* `<class 'list'>` - variable is a list

In python types and classes can be thought of as the same thing, and they
specify what kind of value is contained within a variable.

# Why are types important?

Types (and classes) are useful because they define what kind of operations
you can do with a variable.

```python
a = 5
b = 3
print(a + b) # will print: 8
```

Since both `a` and `b` are of type `<class 'int'>`, python knows that the `+` operator
must do a mathematical addition.


```python
x = "Helo, "
y = "World!"
print(x + y) # will print: "Hello, World!"
```

Since `x` and `y` are of type `<class 'str'>`, the `+` operator will concatenate the 2 strings.

```python
foo = 5
bar = "World!"
print(foo + bar) # will cause an error: TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

The `+` operator cannot be used with an integer and a string, so it will throw an error.

# Function annotation

Types are also useful for annotating function parameters in order to declare
what kind of inputs the function is expecting.

```python
def greet(name: str):
    print("Hello, " + name)
```

Now, everybody who will use this function knows that they should only pass strings to the greet
function. This can prevent issues like passing in variables that would result in errors, like:

```python
greet(5) # would cause error: TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

These annotations are not enforced by python, so you can still have type errors.
However, there are plugins/programs for vs code and other code editors who will do type checking
(verifying that all functions are called with variable of the correct type).

