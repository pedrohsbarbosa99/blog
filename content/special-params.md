---
date: 2025-04-28
tags: python,ti
---

# Special Params

By default, python accepts either position or explicity keywords arguments.

When you want restrict a positional or keyword argument only, you must pass ```/``` for positional only or ```*``` for keyword only.

Positional Argument Only:

```python
def func(pos1, /):
    print(pos1)

## -------------- ##
Argument: func("pos1")
Result: pos1

## -------------- ##
Argument: func(pos1="pos1")
Result: Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: func() missing 1 required positional argument: 'pos1'
```


KeyWord Argument Only:

```python
def func(*, kwd1):
    print(kwd1)

## -------------- ##
Argument: func("pos1", kwd1="kwd1")
Result: pos1 kwd1

## -------------- ##
Argument: func("pos1", "kwd1")
Result: Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: func() takes 1 positional argument but 2 were given
```


In summary, you use can use postional only argument to make name of argument not available for users and keyword only to make the argument more understandable by being explicit with names or don't allow the users trust in position of argument.

For more information, check out:
- <a href="https://docs.python.org/3/tutorial/controlflow.html#positional-or-keyword-arguments" target="_blank">Python Doc</a>

