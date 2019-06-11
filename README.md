# python_advance
begin to learn python

## Table of Contents

- [python_advance](#pythonadvance)
  - [Table of Contents](#table-of-contents)
  - [Using the Python Interpreter](#using-the-python-interpreter)
  - [An Informal Introduction to Python](#an-informal-introduction-to-python)

## Using the Python Interpreter

1 Invoking the Interpreter

1.1 install python and add into path enviroment

(1) installed path

    default installed path is  '/usr/local/bin/python3.6';

(2) exit interpreter

    Typing an end-of-file character (Control-D on Unix, Control-Z on Windows) at the primary prompt causes the interpreter to exit with a zero exit status.

(3) [Command line and environment](https://docs.python.org/3/using/cmdline.html#using-on-general)

1.2 The Interpreter and Its Environment

1.2.1 Source Code Encoding

(1) To declare an encoding other than the default one, a special comment line should be added as the first line of the file. The syntax is as follows:

    ```python
        # -*-: coding: encoding -*-
    ```

## An Informal Introduction to Python

1 Using Python as a Calculator

1.1 Numbers

(1) operators

    +, -, *, /, //, %, = and ()

(2) numeric types

    int, float, Decimal, Fraction, complex(复数);

(3) operators with mixed type operands convert the integer operand to floating point.

(4) the last printed expression is assigned to the variable _

    ```python
        >>> tax = 12.5 / 100
        >>> price = 100.50
        >>> price * tax
        12.5625
        >>> price + _
        113.0625
    ```

1.2 Strings

(1) \ can be used to escape quotes.

(2) Strings can be concatenated (glued together) with the + operator, and repeated with *.

    ```python
        >>> 3 * 'un' + 'ium'
        'unununium'
    ```
(3) Two or more string literals (i.e. the ones enclosed between quotes) next to each other are automatically concatenated.

    ```python
        >>> var = 'Py' 'thon'
        'Python'
    ```

(4) Strings can be indexed

    +---+---+---+---+---+---+
    | P | y | t | h | o | n |
    +---+---+---+---+---+---+
    0   1   2   3   4   5   6
    -6  -5  -4  -3  -2  -1

    ```python
        >>> word = 'Python'
        >>> word[0]  # character in position 0
        'P'
        >>> word[-1]  # last character
        'n'
        >>> word[42]  # the word only has 6 characters
        Traceback (most recent call last):
        File "<stdin>", line 1, in <module>
        IndexError: string index out of range
    ```

**NOTE**: Attempting to use an index that is too large will result in an error.

(5) slicing is also supported

    ```python
        >>> word[0:2]  # characters from position 0 (included) to 2 (excluded)
        'Py'
        >>> word[2:5]  # characters from position 2 (included) to 5 (excluded)
        'tho'
        >>> word[4:42]
        'on'
    ```

**NOTE**: out of range slice indexes are handled gracefully when used for slicing.

(6) Python strings cannot be changed — they are immutable.

    ```python
        >>> word[0] = 'J'
        Traceback (most recent call last):
        File "<stdin>", line 1, in <module>
        TypeError: 'str' object does not support item assignment
    ```

(7) The built-in function len() returns the length of a string:

    ```python
        >>> s = 'supercalifragilisticexpialidocious'
        >>> len(s)
        34
    ```

1.3 Lists

    Lists might contain items of different types, but usually the items all have the same type.

(1) lists can be indexed and sliced

    ```python
        >>> squares = [1, 4, 9, 16, 25]
        >>> squares[0]  # indexing returns the item
        1
        >>> squares[-1]
        25
        >>> squares[-3:]  # slicing returns a new list
        [9, 16, 25]
    ```

(2) Lists also support operations like concatenation:

    ```python
        >>> squares + [36, 49, 64, 81, 100]
        [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
    ```

(3) lists are a mutable type

    ```python
        cubes = [1, 8, 27, 65, 125]
        >>> cubes[3] = 64  # replace the wrong value
        >>> cubes
        [1, 8, 27, 64, 125]
    ```

(4) Assignment to slices is also possible, and this can even change the size of the list or clear it entirely.

(5) The built-in function len() also applies to lists

    ```python
        >>> letters = ['a', 'b', 'c', 'd']
        >>> len(letters)
        4
    ```

(6) It is possible to nest lists (create lists containing other lists)

    ```python
        >>> a = ['a', 'b', 'c']
        >>> n = [1, 2, 3]
        >>> x = [a, n]
        >>> x
        [['a', 'b', 'c'], [1, 2, 3]]
        >>> x[0]
        ['a', 'b', 'c']
        >>> x[0][1]
        'b'
    ```
