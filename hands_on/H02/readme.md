# Estimating $\pi$

In this exercise we will try to estimate the value of $\pi$ numerically.

> every time you want to implement something, it is most likely because you want to answer a question.
> Our question today is:

> **What is $\pi$?**

Before starting to think algorithmically, we want to think scientifically (geometrically?): "what do we know about $\pi$?"

## Deliverable:

* A python script that computes $\pi$ and estimated the error on the computation.
* it would be great to use functions
* it would be great to start by only using the standard python library
* it would be also greater to make the script re-usable and executable with command line arguments

## Hints

* I would test functionalities in a **Jupyter Notebook** or in a **Python shell** (interactive preferably).
  When I am satisfied with what I have learnt, I can copy the relevant commands in the script.

* Do not write a full block of code before testing that it works, it most certanly won't. **GRANULARITY** of functionality testing is essential. 

* The standard python library for random numbers is
  ```python
  import random
  ```
  remember the `dir` command?
  Try to use it to see what functions are contained in the `random` module:
  ```python
  dir(random)
  ```

* Mathematical operations are not only implemented in NumPy, we have a module in the Python Standard Library:
  ```python
  import math
  ```
  note that it is cleaner to import only the functions that you need, e.g.
  ```python
  from math import sqrt
  ```

* We can access system functions with
  ```python
  import sys
  ```
  with wich you can make (e.g.) a script (or an executable) take command line arguments.
  If the script `myscript.py` is
  ```python
  import sys
  print(sys.argv)
  ```
  and I call it with some command line argument (e.g. `42`), I will get:
  ```bash
  $ python myscript.py 42
  [ 'myscript.py', '42' ]
  ```
  so we learn two things:
  * `sys.argv` returns everything that comes after the `python` executable in a list
  * everything is interpreted as a string (like in bash)
  but we can convert it (remember casting?):
  ```python
  argument = int(sys.argv[1])
  ```


