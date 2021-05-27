# Linked List

### Remove Dups

#### Write code to remove duplicates from an unsorted linked list. How would you solve this problem if a temporary buffer is not allowed?

<details>

  <summary>Solution</summary>

- create a hash table or set to store unique integers into it
- run through the linked list and if duplicate is present assign, prev->next = current->next
- for solving the problem without any extra space, we can create a runner pointer which checks for duplicates in the right side for the linked list
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

### Return Kth to Last

#### Implement an algorithm to find the kth to last element of a singly linked list.

<details>

  <summary>Solution</summary>

- Recursive

  - base case is where head == null
  - check in which recursive call index == k, return that node
  - Time Complexity is, $O(n)$
  - Space Complexity is, $O(n)$

- Iterative
  - We can use two pointers, p1 and p2 both refering to head initially
  - move p1 to k nodes after head
  - iterate until p1 hits null
  - p2 will be at the kth to the last position in the linked list
  - Time Complexity is, $O(n)$
  - Space Complexity is, $O(1)$

</details>

### Delete Middle Node

#### Implement an algorithm to delete a node in the middle (i.e., any node but the first and last node, not necessarily the exact middle) of a singly linked list, given only access to that node.

<details>

  <summary>Solution</summary>

- copy the data from the delete_node.right to the delete_node
- delete the node delete_node.right
- Time Complexity is, $O(1)$
- Space Complexity is, $O(1)$

</details>

### Partition

#### Write code to partition a linked list around a value x, such that all nodes less than x come before all nodes greater than or equal to x. If x is contained within the list, the values of x only need to be after the elements less than x. The partition element x can appear anywhere in the 'right parition'; it does not need to appear between the left and right partitions.

<details>

  <summary>Solution</summary>

- create head and tail pointer
- iterate through the linked list, if node.value is less than pivot.value make it the new head otherwise append it to the tail pointer
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

### Sum Lists

#### You have two numbers represented by a linked list, where each node contains a single digit. The digits are stored in reverse order, such that the 1's digit is at the head of the list. Write a function that adds the two numbers and returns the sum as a linked list. FOLLOW UP. Suppose the digits are stored in forward order. Repeat the above problem.

<details>

  <summary>Solution</summary>

- Reverse Order
  - iterate through the both of the linked lists
  - add the digits along with the carry
  - return the head
  - Time Complexity is, $O(n)$
  - Space Complexity is, $O(n)$

</details>

### Palindrome

#### Implement a function to check if a linked list is a palindrome.

<details>

  <summary>Solution</summary>

- use two fast and slow pointer method to get to the middle element
- push the elements of the slow pointer on the stack
- after reaching end, check for even and odd situation
  - if fast pointer is at the end, then even
  - otherwise odd
- pop elements from the stack and check with slow pointer's value
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

### Intersection

#### Given two (singly) linked lists, determine if the two lists intersect. Return the intersecting node. Note that the intersection is defined based on reference, not value. That is, if the kth node of the first linked list is the exact same node (by reference) as the jth node of the second linked list, they they are intersection.

<details>

  <summary>Solution</summary>

- get the lengths of the linked lists
- create two pointers and assign them to the head of the linked lists
- offset the pointer which is assigned to the bigger linked list by abs(len(ll1) - len(ll2))
- iterate through the linked list one node at a time
- if both the node referece match for the pointers, return that Node
- otherwise, return None
- Time Complexity is, $O(A + b)$
- Space Complexity is, $O(1)$

</details>

### Loop Detection

#### Given a circular linked list, implement an algorithm that returns the node at the beginning of the loop.
