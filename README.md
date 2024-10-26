# Binary Search in Java

This repository contains a Java implementation of the binary search algorithm. The program prompts the user to enter a sorted array and then searches for a specified element using binary search. 

## How It Works
1. The user enters the number of elements in the array.
2. The user provides the sorted elements.
3. The user inputs the element to search for.
4. The binary search function checks if the element exists in the array:
   - If found, it displays the index of the element.
   - If not, it notifies the user that the element is not in the array.

## Code Description
- **Package:** `com.mycompany.test`
- **Imports:**
  - `Scanner`: Used for reading input from the user.
  - `Arrays`: Provides utility methods for array operations.
- **Functionality:** 
  - `binarySearch(int[] arr, int key)`: Executes binary search on the given array to locate the specified key.
  - `main`: Collects input, sorts the array, and calls `binarySearch` to display the result.

## Example
Input:
