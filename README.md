Lab  - Advanced Logger
======================

You will implement your own C logger library, it's going to be divided in 2 parts:
- Part 1 - in-`stdout` logging
- Part 2- in-`syslog` logging

It's important to know that this library will be ONLY used in Linux-based systems, since we'll be using the `syslog`.

Part 1 - stdout logging
-----------------------

Implement a Logger library in C that will be used for printing the following types of messages.

- `INFO` General information.
- `WARN` Warnings.
- `ERROR` Errors.
- `PANIC` Panics. Non recoverable issues with core dump.

This logger library will be used instead of printf function calls in all new labs and challenges that we'll be doing in the course. Below you can see the prototype for each function.


From now, all your C programs must use this logger for displaying
messages in the console, instead of common `printf` function calls.

Part 2 - syslog logging
-----------------------

A new `initLogger`function will be added in order to add support for
choosing between `stdout` or `syslog` logging.

```
int initLogger(char *logType)
```

You will handle the following log types:
- `stdout` or empty string for `STDOUT` logging
- `syslog` for `SYSLOG` logging

Use the **The Linux Programming Interface** book as a
reference for your implementation. See *37th chapter on 5th section*.

General Instructions
--------------------
- Use the `testLogger.c` file for testing your `logger.c` library implementation.
- You can update the `Makefile` for your compilation and linking.
- Update `README.md` with the proper steps for building and running your code.
- Don't forget to handle errors properly.
- Coding best practices implementation will be also considered.

Test Suite
----------
Build and Test automation is already implemented with the following command. Below some general tips and comments.

- Make sure that your program passes all test cases without errors.
- Remember that this is being executed by a robot script.
- You cannot edit the `lab.mk` file.
- Failed compilation or segmentation faults means 0-graded.
- Failed tests without proper handling  will be properly discounted from total grade.

```
make test
```
