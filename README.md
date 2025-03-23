Question One
Big O notation is used to describe the time complexity or space complexity of an algorithm. It provides an upper bound on the growth rate of an algorithm's runtime or memory usage as the input size increases. Below are the key rules of Big O notation with examples:

1. Constant Time - O(1):
   - The algorithm's runtime does not depend on the input size.
   - Example: Accessing an element in an array by index.
     java
     int getElement(int[] arr, int index) {
         return arr[index]; // O(1)
     }

2. Linear Time - O(n):
   - The algorithm's runtime grows linearly with the input size.
   - Example: Iterating through an array.
     java
     void print Array(int[] arr) {
         for (int i = 0; i < arr.length; i++) { // O(n)
             System.out.println(arr[i]);
         }
     }

3. Quadratic Time - O(n²):
   - The algorithm's runtime grows proportionally to the square of the input size.
   - Example: Nested loops.
     java
     void printPairs(int[] arr) {
         for (int i = 0; i < arr.length; i++) { // O(n)
             for (int j = 0; j < arr.length; j++) { // O(n)
                 System.out.println(arr[i] + ", " + arr[j]);
             }
         }
     }

4. Logarithmic Time - O(log n):
   - The algorithm's runtime grows logarithmically with the input size.
   - Example: Binary search.
     java
     int binarySearch(int[] arr, int target) {
         int left = 0, right = arr.length - 1;
         while (left <= right) { // O(log n)
             int mid = left + (right - left) / 2;
             if (arr[mid] == target) return mid;
             if (arr[mid] < target) left = mid + 1;
             else right = mid - 1;
         }
         return -1;
     }

5. Linearithmic Time - O(n log n):
   - The algorithm's runtime grows in proportion to `n log n`.
   - Example: Merge sort or quicksort.
     java
     void mergeSort(int[] arr) {
         // Implementation of merge sort (O(n log n))
     }

6. Drop Non-Dominant Terms:
   - When analyzing complexity, drop non-dominant terms.
   - Example: `O(n² + n)` simplifies to `O(n²)`.

7. Ignore Constants:
   - Constants are ignored in Big O notation.
   - Example: `O(2n)` simplifies to `O(n)`.
Question Two
Arrays vs. Linked Lists

Arrays and linked lists are two fundamental data structures with clear characteristics. Below is a comparison based on memory allocation, performance, and insertion/deletion operations:

1. Memory Allocation:
   Arrays:
     - Contiguous memory allocation.
     - Fixed size (static arrays) or dynamic size (dynamic arrays).
     - Requires a single block of memory.
    Linked Lists:
     - Non-contiguous memory allocation.
     - Each node contains data and a pointer to the next node.
     - Memory is allocated dynamically as nodes are added.

2. Performance:
    Arrays:
     - Fast access to elements by index (O(1)).
     - Slower insertion/deletion in the middle (O(n)) due to shifting elements.
    Linked Lists:
     - Slower access to elements by index (O(n)) due to traversal.
     - Faster insertion/deletion at the beginning or end (O(1) for singly linked lists).

3. Insertion and  Deletion Operations:
   Arrays:
     - Insertion/deletion at the beginning or middle requires shifting elements, making it O(n).
     - Insertion at the end is O(1) if space is available; otherwise, resizing is required.
    Linked Lists:
     - Insertion/deletion at the beginning is O(1).
     - Insertion/deletion at the end is O(1) if a tail pointer is maintained; otherwise, O(n).
     - Insertion/deletion in the middle requires traversal, making it O(n).
