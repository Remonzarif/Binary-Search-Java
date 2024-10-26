// Hi, this code demonstrates a binary search using an array
package com.mycompany.test;

import java.util.Scanner; // Importing Scanner class to take input from user 
import java.util.Arrays;  // Importing Arrays class to use array-related methods 

public class Test {
    // Method to perform binary search
    static int binarySearch(int arr[], int key) {
        int left = 0;
        int right = arr.length - 1;
        
        while (left <= right) { // While the left index is less than or equal to right
            int mid = left + (right - left) / 2; // Calculate the middle index

            if (arr[mid] == key) { // If the middle element is the key, return index
                return mid;
            }
            if (arr[mid] > key) {  // If key is smaller than mid element, adjust the right boundary
                right = mid - 1;
            } else {               // If key is larger, adjust the left boundary
                left = mid + 1;
            }
        }
        return -1; // If the key is not found, return -1
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.println("Enter the number of elements: ");
        int n = input.nextInt();
        
        int[] arr = new int[n]; // Create an array of size n
        System.out.println("Enter the elements (sorted): ");
        for (int i = 0; i < n; i++) {
            arr[i] = input.nextInt(); // Read each element from user into the array
        }
        
        System.out.println("Enter the element to search for: ");
        int key = input.nextInt();
        
        Arrays.sort(arr); // Sort the array (in case it's not already sorted)
        int result = binarySearch(arr, key); // Perform binary search
        
        if (result == -1) {
            System.out.println("The element was not found.");
        } else {
            System.out.printf("The element was found at index: %d", result);
        }
    }
}
