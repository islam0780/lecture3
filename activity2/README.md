# Activities

## Task 1

- Refer to the following link. Discuss how Insertion works:
  https://opendsa-server.cs.vt.edu/ODSA/AV/Sorting/insertionsortAV.html
  
// Insertion sort is a simple sorting algorithm that works by dividing the input into two parts: the sorted part and the unsorted part. The algorithm starts by considering the first element as the only sorted item and the rest of the elements as the unsorted part.

In each iteration, the algorithm takes the first unsorted element, compares it to the sorted elements, and finds its proper place among the sorted elements by shifting the larger elements to the right. The algorithm then inserts the element in its proper place and repeats this process for the rest of the unsorted elements.

The algorithm continues until all elements are sorted, which means the sorted part contains all the elements in the correct order. The sorting process takes O(n^2) time in the worst case but it has a better performance in the average case, especially when the input is partially sorted.

## Task 2

- The following snippet is from `./src/insertion.cpp` lines 12-22. Discuss in groups how the code works:

```cpp
    for (int k = 1; k < 10; k++)
    {
        int temp = myarray[k];
        int j = k - 1;
        while (j >= 0 && temp <= myarray[j])
        {
            myarray[j + 1] = myarray[j];
            j = j - 1;
        }
        myarray[j + 1] = temp;
    }
```
//
 The code above implements the Insertion Sort algorithm. The outer loop for (int k = 1; k < 10; k++) starts with the second element of the input array myarray (index 1) and goes until the last element (index 9).

The inner loop while (j >= 0 && temp <= myarray[j]) moves the elements of the sorted part to the right, to make room for the current unsorted element, temp, which is equal to myarray[k]. This loop continues until it finds the correct place for temp or until it reaches the start of the sorted part.

The inner loop decrements j by one in each iteration until it finds the correct place for temp or it reaches the start of the sorted part.

Finally, the current unsorted element temp is placed in its proper place by the line myarray[j + 1] = temp. The outer loop then continues with the next unsorted element.

The algorithm continues until all elements are sorted, which means the sorted part contains all the elements in the correct order.

## Task 3

- Discuss the complexity analysis of insertion sort. Refer to the link below:
  https://www.softwaretestinghelp.com/insertion-sort/

// The time complexity of Insertion Sort is O(n^2) in the worst case scenario, where n is the number of elements in the input array. This happens when the input is in the reverse order and the algorithm has to compare and shift each element to its proper place. In the worst case, the algorithm takes n-1 comparisons and n-1 shifts for each of the n elements, resulting in a time complexity of O(n^2).

However, Insertion Sort has a better average-case time complexity than other O(n^2) algorithms, such as selection sort, when the input is partially sorted. In this case, the algorithm takes advantage of the partial ordering and requires fewer comparisons and shifts, resulting in a faster performance.

The space complexity of Insertion Sort is O(1), as it only requires a constant amount of additional memory to store temporary variables, regardless of the size of the input.

Insertion Sort is a simple and easy to understand sorting algorithm that is well suited for small arrays and for partially sorted arrays. However, for large arrays or arrays that are not partially sorted, other sorting algorithms, such as Quicksort or Merge Sort, are more efficient.

## Links

- https://cpp.sh/
