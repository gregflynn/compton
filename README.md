test.h
======

A very simple, light weight, header only C unit test framework.

## Features

* Easy to use, no dependencies, no setup needed.
* Keep test cases close to the code they test.
* Automatic registration of the test cases.

## Setup

Just include the header

```c
#include "test.h"
```

To enable the test cases in your code, compile your program with `-DUNIT_TEST`.

## Defining test cases

```c
TEST_CASE(test_case_name) {
	// Your code here
	// ...
	SHOULD_EQUAL(1, 0); // Fail
}
```

## Run the test cases

In your main function, call `run_tests`:

```c
int main() {
	// necessary setup code
	// ...
#ifdef UNIT_TEST
	run_tests();
	// cleanup
#endif
	// usual code
}

```
