---
metaTitle: "Python - Raise Custom Errors / Exceptions"
description: "Custom Exception, Catch custom Exception"
---

# Raise Custom Errors / Exceptions


Python has many built-in exceptions which force your program to output an error when something in it goes wrong.

However, sometimes you may need to create custom exceptions that serve your purpose.

In Python, users can define such exceptions by creating a new class. This exception class has to be derived, either directly or indirectly, from Exception class. Most of the built-in exceptions are also derived from this class.



## Custom Exception


Here, we have created a user-defined exception called CustomError which is derived from the Exception class. This new exception can be raised, like other exceptions, using the raise statement with an optional error message.

```py
class CustomError(Exception):
       pass

x = 1

if x == 1:
    raise CustomError('This is custom error')

```

Output:

```py
Traceback (most recent call last):
  File "error_custom.py", line 8, in <module>
    raise CustomError('This is custom error')
__main__.CustomError: This is custom error

```



## Catch custom Exception


This example shows how to catch custom Exception

```py
class CustomError(Exception):
     pass

try:
    raise CustomError('Can you catch me ?')
except CustomError as e:
    print ('Catched CustomError :{}'.format(e))
except Exception as e:
    print ('Generic exception: {}'.format(e))

```

Output:

```py
Catched CustomError :Can you catch me ?

```

