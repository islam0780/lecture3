# Activities

## Task 1

- Refer to the following link. Discuss how bubble sort works:
  https://opendsa-server.cs.vt.edu/embed/bubblesortAV

  //
Bubble sort is a simple sorting algorithm that works by repeatedly swapping adjacent elements if they are in the wrong order until the list is sorted. In each pass through the list, the largest unsorted element "bubbles up" to its correct position at the end of the list. The process continues by reducing the length of the unsorted portion of the list and repeating the steps until the entire list is sorted. This algorithm has a time complexity of O(n^2) in the worst-case scenario, making it inefficient for large lists, but it is easy to understand and implement.

## Task 2

- Refer to the following link. Your task is to show the behavior for one iteration of the outer for loop of Bubble Sort (Try at least 3 cases).
  https://opendsa-server.cs.vt.edu/ODSA/Exercises/Sorting/BubsortPRO.html

## Task 3

- The following snippet is from `./src/bubble.cpp` lines 16-28. Discuss in groups how the code works:

```cpp

    for (i = 0; i < 10; i++)
    {
        for (j = i + 1; j < 10; j++)
        {
            if (a[j] < a[i])
            {
                temp = a[i];
                a[i] = a[j];
                a[j] = temp;
            }
        }
        pass++;
    }
```
// This code implements the Bubble Sort algorithm to sort an array of integers in ascending order.

The outer for loop (line 17) with i as its control variable is used to traverse the array and perform the sorting operation in multiple passes. The loop runs 10 times, which is the length of the array a.

The inner for loop (line 19) with j as its control variable is used to compare each pair of adjacent elements in the array. The variable j starts from i + 1 to avoid comparing an element with itself. The loop runs 10 times, which is the length of the array a.

The if statement (line 21) compares the value of the element at index j with the value of the element at index i. If the value of the element at index j is less than the value of the element at index i, a swap is performed. A temporary variable temp is used to store the value of the element at index i before it is swapped with the value of the element at index j.

The number of passes (i.e., the number of times the outer for loop has been executed) is incremented with each iteration of the outer loop (line 26).

The end result is that the array a is sorted in ascending order.

- The following snippet is from `./src/selection.cpp` lines 34-41. Discuss in groups how the code works:

```cpp
    for (j = i + 1; j < 10; j++)
    {
        if (myarray[j] < ele_small)
        {
            ele_small = myarray[j];
            position = j;
        }
    }
```
//
This code implements the selection sort algorithm, specifically it finds the minimum element in the unsorted portion of the array myarray.

The for loop (line 36) with j as its control variable is used to traverse the unsorted portion of the array myarray starting from the next index after the current index i. The loop runs 10 times, which is the length of the array myarray.

The if statement (line 38) compares the value of the element at index j with the value of the current minimum element stored in the variable ele_small. If the value of the element at index j is less than the value of ele_small, the value of ele_small is updated with the value of the element at index j and the position of the minimum element is stored in the variable position.

The end result is that the minimum element in the unsorted portion of the array is found and its position is stored in the variable position.

## Task 4: Individual, at home

- Discuss the complexity analysis of selection sort. Refer to the link below:
  https://www.softwaretestinghelp.com/selection-sort/

## Links

- https://cpp.sh/
