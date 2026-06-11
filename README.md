# Python Makefile Interpreter

> [!WARNING]
> this is a very early version and an unstable prototype

Simple makefile interpreter, which can (for now) only work with simple instructions and global variables. Does not evaluate changes in files.

Good for simple usecases.

## Usage

Create a Makefile.

Example:

```Makefile
hello: test.cpp
	echo Hello $(what)

what := World


test: test.cpp
	g++ $(CXX_FLAG) test.cpp -o test.exe
	test.exe

CXX_FLAG := -std=c++11
```
Execute the Makefile with

```Bash
python makefile.py <instruction>
```

Example:

```Bash
python makefile.py test
```

## Error Logging

```Makefile
what = World
```
```
Unsupported Syntax. Did you forget a ":"?
what = World
    ^
Makefile terminated.
```
