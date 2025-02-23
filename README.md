# ConcurrentModificationException in Kotlin List Iteration

This example demonstrates a common error in Kotlin involving the `ConcurrentModificationException`. This exception occurs when you modify a collection (like a `MutableList`) while iterating over it using a traditional `for` loop.

The code shows how to use `removeIf` safely with `MutableList` and `MutableSet`, and the error you get if you try to modify a `MutableList` during iteration using a traditional for loop.

## How to Reproduce

Run the `bug.kt` file. The `for` loop example will throw a `ConcurrentModificationException`, while the `removeIf` examples work correctly.

## Solution

The solution is to avoid directly modifying the list while iterating. Use `removeIf` for safe removal, or create a copy of the list for safer modification.