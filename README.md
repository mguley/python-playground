## Python Playground

A hands-on learning environment for Python internals, performance optimization, and advanced programming patterns. 
This repository contains practical scenarios that demonstrate Python's runtime behavior, memory management, concurrency models, and metaprogramming capabilities through guided exercises.

## Overview

This playground is designed to help you understand Python at a deeper level by exploring its implementation details and advanced features. 
Each scenario focuses on a specific aspect of Python's runtime behavior or language feature that is crucial for writing efficient, maintainable Python code in production environments.
Unlike typical Python tutorials that focus on syntax and basic usage, these scenarios dive into the "why" and "how" of Python's design decisions, helping you write better code by understanding what happens under the hood.

## Prerequisites

Before starting, ensure you have the following installed:

- [Python](https://www.python.org/downloads/) (version 3.12+ recommended)
- pip (Python package installer)
- A code editor with Python support (VS Code, PyCharm, or similar)
- Basic understanding of Python syntax and programming concepts
- Familiarity with command-line tools

For some advanced scenarios, you may also need:
- C compiler (for C extension scenarios)
- Python development headers (`python3-dev` on Ubuntu/Debian)

## Getting Started

```bash
# Clone this repository
git clone https://github.com/mguley/python-playground.git
cd python-playground

# View available scenarios
ls -la
```

## Available Scenarios

### [Scenario 1: Python's Memory Management and Reference Counting](./scenario-01-memory-management/)

Explore how Python manages memory through reference counting and garbage collection. 
This scenario demonstrates the fundamental differences between Python and compiled languages like Go, showing how objects are allocated, tracked, and freed in the CPython runtime.

**Key Topics:**
- Reference counting mechanism and `sys.getrefcount()`
- Circular references and garbage collector behavior
- Memory profiling with `tracemalloc` and `memory_profiler`
- Weak references and memory optimization patterns
- Object pooling strategies in Python

### [Scenario 2: Python Bytecode and the CPython Virtual Machine](./scenario-02-bytecode-and-vm/)

Understand how Python code is compiled to bytecode and executed by the CPython virtual machine. 
This scenario demystifies Python's execution model and shows how different coding patterns affect performance at the bytecode level.

**Key Topics:**
- Using the `dis` module to examine bytecode
- Understanding the Python evaluation stack
- Bytecode optimization patterns
- Performance implications of different Python constructs
- Writing a simple bytecode optimizer

### [Scenario 3: The Import System and Module Loading Mechanics](./scenario-03-import-system/)

Master Python's sophisticated import system and module loading mechanism. 
This scenario reveals how Python finds and loads modules, enabling you to build plugin systems and understand complex package structures.

**Key Topics:**
- Import hooks and custom importers
- The module search path and `sys.modules`
- Namespace packages and `__init__.py` files
- Circular imports and lazy loading strategies
- Building a plugin architecture using import machinery

### [Scenario 4: Context Managers and Resource Management](./scenario-04-context-managers/)

Learn Python's approach to resource management through context managers. 
This scenario compares Python's `with` statement to Go's `defer` and demonstrates how to implement robust resource handling patterns.

**Key Topics:**
- The context manager protocol (`__enter__` and `__exit__`)
- Using `contextlib` for simpler context managers
- Exception handling in context managers
- Reentrant and reusable context managers
- Asynchronous context managers for async resources

### [Scenario 5: The Descriptor Protocol and Property Implementation](./scenario-05-descriptors/)

Dive deep into Python's descriptor protocol to understand how properties, methods, and attribute access work internally. 
This scenario reveals the magic behind Python's object model.

**Key Topics:**
- Understanding descriptors and the descriptor protocol
- Implementing custom properties and validators
- Method resolution order (MRO) and `super()`
- Building lazy properties and cached attributes
- Descriptors vs. `__getattr__` and `__getattribute__`

### [Scenario 6: Metaclasses and Dynamic Class Creation](./scenario-06-metaclasses/)

Explore Python's powerful metaprogramming capabilities through metaclasses. 
This scenario demonstrates how to customize class creation and implement advanced patterns used by popular frameworks.

**Key Topics:**
- Understanding `type` and class creation
- Writing custom metaclasses
- Class decorators vs. metaclasses
- Practical applications: ORMs and serialization
- Abstract base classes and interface enforcement

### [Scenario 7: Generator Functions and the Evolution to Coroutines](./scenario-07-generators-coroutines/)

Trace Python's journey from simple generators to modern async/await. 
This scenario provides historical context and deep understanding of Python's concurrency evolution.

**Key Topics:**
- Iterator protocol and generator functions
- Generator expressions and memory efficiency
- Coroutines with `yield from`
- The transition from generator-based to native coroutines
- Building a simple task scheduler

### [Scenario 8: Event Loops in Python](./scenario-08-event-loops/)

Understand how event loops power asynchronous Python applications. 
This scenario builds a simplified event loop from scratch to demonstrate the core concepts behind `asyncio`.

**Key Topics:**
- Event loop architecture and design patterns
- Callbacks, futures, and tasks
- Building a minimal event loop
- Understanding `asyncio`'s event loop implementation
- Integration with blocking I/O and thread pools

### [Scenario 9: Async/Await and Modern Asynchronous Python](./scenario-09-async-await/)

Master modern asynchronous programming in Python with async/await. 
This scenario covers practical patterns and common pitfalls in async Python development.

**Key Topics:**
- Native coroutines and the `async`/`await` syntax
- Asynchronous context managers and iterators
- Concurrency patterns: gather, wait, and as_completed
- Error handling in asynchronous code
- Performance comparison: sync vs. async approaches

### [Scenario 10: The Global Interpreter Lock (GIL) and True Parallelism](./scenario-10-gil-parallelism/)

Confront Python's most famous limitation and learn how to achieve true parallelism. 
This scenario demonstrates the GIL's impact and explores various workarounds for CPU-bound tasks.

**Key Topics:**
- Understanding the GIL and its implications
- Threading vs. multiprocessing in Python
- Using `concurrent.futures` for parallel execution
- Shared memory and inter-process communication
- Alternative Python implementations (PyPy, Jython)

### [Scenario 11: Type Hints and Runtime Type Checking](./scenario-11-type-hints/)

Explore Python's gradual typing system and its runtime applications. 
This scenario shows how type hints can improve code quality and enable powerful runtime validations.

**Key Topics:**
- Type annotations and the `typing` module
- Runtime type checking with decorators
- Generic types and type variables
- Protocol classes and structural subtyping
- Building type-safe APIs with runtime validation

### [Scenario 12: C Extensions and Performance Optimization](./scenario-12-c-extensions/)

Learn when and how to drop down to C for performance-critical code. 
This scenario demonstrates various approaches to extending Python with compiled code.

**Key Topics:**
- Writing Python C extensions
- Using Cython for easier C integration
- CFFI and ctypes for foreign function interfaces
- Profiling and identifying optimization candidates
- Benchmarking Python vs. C extension performance
