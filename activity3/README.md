# Activities

## Task 1:

- Refer to the following link. Discuss how Queues based on linked lists works:
  https://www.cs.usfca.edu/~galles/visualization/QueueLL.html

//A queue based on linked lists is a linear data structure where elements are added at the back (also called enqueue operation) and removed from the front (also called dequeue operation). This operation mimics a real-life queue, where people wait in line for their turn.

A linked list-based queue is implemented by using a linked list to store the elements. Each node in the linked list contains the value of an element and a reference to the next node in the list. The front of the queue is represented by the head of the linked list, while the back of the queue is represented by the tail.

When a new element is added to the queue, it is added as a new node at the end of the linked list (tail). When an element is removed from the queue, the head node is removed and its reference to the next node becomes the new head of the linked list.

Linked list-based queues have dynamic size, meaning they can grow or shrink as needed, and do not have the limitations of arrays in terms of size. They also allow for constant-time enqueue and dequeue operations, as adding or removing elements only requires updating the references to the head and tail nodes.

In summary, linked list-based queues provide a flexible and efficient way of implementing a queue, where elements are added at the back and removed from the front in a first-in-first-out (FIFO) manner.

## Task 2:

- The following snippet is from `./src/queue.cpp` lines 8-10. What happens if `front`, `rear` and `temp` were not global variables?

```cpp
struct node *front = NULL;
struct node *rear = NULL;
struct node *temp;
```
// If the variables front, rear, and temp were not global variables, they would only be accessible within the scope in which they were declared, likely the function in which they appear. This would mean that any other function that needs to access these variables would not be able to do so, as it would only have access to its own local variables.

For example, if the code needed to enqueue an element in the queue and access rear to update it, this would not be possible if rear were not a global variable. The same would apply to any other operation that requires access to these variables, such as dequeueing an element or traversing the queue.

By making these variables global, they are accessible from any part of the code, which allows for a more flexible and maintainable implementation of the queue.

## Task 3:

- The following snippet is from `./src/queue.cpp` lines 11-28. Discuss in groups how the code works:

```cpp
void Insert(int val)
{
    if (rear == NULL)
    {
        rear = new node;
        rear->next = NULL;
        rear->data = val;
        front = rear;
    }
    else
    {
        temp = new node;
        rear->next = temp;
        temp->data = val;
        temp->next = NULL;
        rear = temp;
    }
}
```
//This code implements the enqueue operation for a linked list-based queue. The Insert function takes an integer val as an argument, which is the value of the element to be added to the queue.

The function starts by checking if the rear pointer is equal to NULL, which means that the queue is empty. If this is the case, the code creates a new node using the new operator, sets its data field to val, and sets its next field to NULL. The rear pointer is then set to point to this new node, and front is also set to point to this node, since the queue now has only one element.

If the queue is not empty, the code creates a new node and sets its data field to val and its next field to NULL. The next field of the current rear node is set to point to this new node, and the rear pointer is updated to point to the new node.

In this way, the code implements the enqueue operation, adding a new node to the back of the linked list, which represents the queue. The rear pointer always points to the last node in the linked list, which is the back of the queue, and the front pointer always points to the first node in the linked list, which is the front of the queue.

## Task 4: Individual, at home

- Discuss the various operations that can be performed on a linked list. Refer to the following link:
  https://www.softwaretestinghelp.com/linked-list/

// A linked list is a data structure that consists of a sequence of nodes, where each node contains a data element and a reference to the next node in the list. Linked lists are a dynamic data structure, which means that the number of elements in the list can change during runtime.

The following are the common operations that can be performed on a linked list:

Insertion: Adding a new node to the list at the beginning, end, or any specific position.

Deletion: Removing a node from the list, based on its value or position.

Traversal: Visiting each node in the list, one after the other, to access its data.

Search: Finding a node in the list, based on its value.

Reverse: Reversing the order of nodes in the list.

Sorting: Arranging the nodes in the list in a specific order, based on their values.

Merging: Combining two linked lists into a single list.

Splitting: Separating a linked list into two or more smaller linked lists.

These operations can be performed using various algorithms and techniques, depending on the specific requirements of the problem being solved. However, it's important to note that some operations, like inserting and deleting elements, can have different time and space complexities based on the location where the operation is performed in the list.

## Links

- https://cpp.sh/
