# C++ STL List Implementation

This project implements a custom list container in C++ that uses a doubly-linked list as its underlying data structure. The implementation follows the interface of std::list while providing a robust foundation for list operations with comprehensive memory management.

## Overview

The custom list is implemented through a template class with an underlying Node structure that supports bidirectional linking. Key features include:

- Template-based implementation supporting any data type
- Custom allocator support
- Doubly-linked structure with previous and next pointers
- Memory-efficient node management
- Support for both copy and move semantics
- STL-compatible iterator implementation

## Class Structure

### `list<T, A>`
The main list class template with two parameters:
- T: Type of elements stored in the list
- A: Allocator type (defaults to std::allocator<T>)

### `Node`
Internal node structure containing:
- `data`: The stored element
- `pNext`: Pointer to the next node
- `pPrev`: Pointer to the previous node

### `iterator`
Custom bidirectional iterator class supporting:
- Forward and backward traversal
- Standard iterator operations (++, --, *, ==, !=)
- STL container compatibility

## List Operations

The implementation includes standard list operations:

### Element Access
- `front()`: Access first element
- `back()`: Access last element

### Modifiers
- `push_front()`: Insert element at beginning
- `push_back()`: Insert element at end
- `pop_front()`: Remove first element
- `pop_back()`: Remove last element
- `insert()`: Insert element at position
- `erase()`: Remove element at position
- `clear()`: Remove all elements
- `swap()`: Exchange contents with another list

### Capacity
- `empty()`: Check if list is empty
- `size()`: Get number of elements

### Construction/Assignment
- Default constructor
- Size constructor
- Range constructor
- Copy constructor
- Move constructor
- Initializer list constructor
- Assignment operators (copy, move, initializer list)

## Usage Example

```cpp
#include "list.h"

// Create a list of integers
custom::list<int> myList;

// Add elements
myList.push_back(1);
myList.push_front(0);
myList.push_back(2);

// Iterate through the list
for (auto it = myList.begin(); it != myList.end(); ++it)
    std::cout << *it << " ";

// Use range-based for loop
for (const auto& item : myList)
    std::cout << item << " ";
```

## Memory Management

- Efficient node allocation using custom allocator support
- Proper cleanup in destructors and clear operations
- Prevention of memory leaks in all operations
- Exception-safe operations

## Files

- `list.h`: Main list implementation with Node and iterator classes
- Unit tests (not included in repository)

## Building

The project includes Visual Studio solution files for building on Windows. Open `LabList.sln` and build using Visual Studio 2019 or later.

## Notes

- This is an educational implementation demonstrating list container concepts
- The implementation closely follows the std::list interface
- Special attention is paid to memory management and exception safety
- Supports both forward and backward traversal through bidirectional iterators

## License

This code is provided for educational purposes. See included license file for terms of use.

## Authors

Nathan Bird  
[nathanbirdka@gmail.com](mailto:nathanbirdka@gmail.com)

Brock Hoskins  
[]()