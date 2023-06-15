---
layout: post
title: "Challenge 1 - Crow's Nest"
description: "For meeting Wednesday 14th June"
author: Andy Baxter
---

This challenge is from the [Tiny Python Projects](http://tinypythonprojects.com/) book and can be tackled in a language of your choice. We'll meet on the 19th of July to compare answers!

## Clubbers' submissions on GitHub:

| Coder | Language | Repo |
|-------|----------|------|
| Andy Baxter | Java | [Java_crows_nest](https://github.com/andrewbaxter439/Java_crows_nest) |


# Crow's Nest Challenge brief

From [the Tiny Python Projects repo](https://github.com/kyclark/tiny_python_projects/tree/master/02_crowsnest)
[YouTube tutorial](https://www.youtube.com/playlist?list=PLhOuww6rJJNPBqIwfD-0RedqsitBliLhT)

Write a program that will announce the appearance of something "off the larboard bow" to the captain of the ship.
Note that you need to "a" before a word starting with a consonant:

```
$ ./crowsnest.py narwhal
Ahoy, Captain, a narwhal off the larboard bow!
```

Or "an" before a word starting with a vowel:

```
$ ./crowsnest.py octopus
Ahoy, Captain, an octopus off the larboard bow!
```

Given no arguments, the program should print a brief usage:

```
$ ./crowsnest.py
usage: crowsnest.py [-h] str
crowsnest.py: error: the following arguments are required: str
```

It should print a longer usage for `-h` and `--help`:

```
$ ./crowsnest.py -h
usage: crowsnest.py [-h] str

Crow's Nest -- choose the correct article

positional arguments:
  str         A word

optional arguments:
  -h, --help  show this help message and exit
```

A passing test suite looks like this:

```
$ make test
pytest -xv test.py
============================= test session starts ==============================
...
collected 6 items

test.py::test_exists PASSED                                              [ 16%]
test.py::test_usage PASSED                                               [ 33%]
test.py::test_consonant PASSED                                           [ 50%]
test.py::test_consonant_upper PASSED                                     [ 66%]
test.py::test_vowel PASSED                                               [ 83%]
test.py::test_vowel_upper PASSED                                         [100%]

============================== 6 passed in 2.89s ===============================
```
