# Stack and Queues

### Three in One

#### Describe how you could use a single array to implement three stacks.

<details>

  <summary>Solution</summary>

- use sizes array to store the current size of each stack
- use array to store the elements in the three stacks
- use top_index(stack_no) to find out the top index of each stack
- implement, push, pop, peek and is_empty like a stack

</details>

### Stack Min.

#### How would you design a stack which, in addition to push and pop, has a function min which returns the minimum element? push, pop, and min should all operate in $O(1)$ time.

<details>

  <summary>Solution</summary>

1. We could store min for each value in the stack while pushing.

2. We can create a new stack inside the class.
   - we push in the min stack, if the stack is empty or the element to be pushed is smaller the the top min stack
   - we pop the element from the min stack if the element is equal to the element we are popping out from the main stack

</details>

### Stack of Plates

#### Imagine a stack of plates. If the stack gets too high, it might topple. Therefore, in real life, we would likely to start a new stack when the previous stack exceeds some threshold. Implement a data structure set_of_stacks that mimics this. set_of_stacks should be composed of several stacks and should create a new stack once the previous one exceeds capacity. set_of_stacks.push() and set_of_stacks.pop() should behave identically to a single stack.

<details>

  <summary>Solution</summary>

- we have to use an array of stacks.
- check the last stack, if it is full, create a new stack and push it to the array of stacks
- check for the same while popping an element from the array of stacks

</details>

### Queue via Stacks

#### Implement a MyQueue class which implements a queue using two stacks

<details>

  <summary>Solution</summary>

- we can create two stacks new_stack, old_stack
- when pushing, we push it into the new_stack
- when popping, we pop if from the old_stack, if it is empty, we pop all the elements first from the new_stack and push it to the old_stack and perform a single pop operation from the old_stack

</details>

### Sort Stack

#### Write a program to sort a stack such that the smallest items are on the top. You can use an additional temporary stack, but you may not copy the elements into any other data structure (such as an array). The stack supports the following operations: push, pop, peek, and is_empty.

<details>

  <summary>Solution</summary>

- create another stack which would store the elements from top in descending order
- while stack is not empty, pop the element from the original stack and store it into a variable
- while new stack is peek > element, pop element and push it to the original stack
- now pop all the elements and push it to the original stack
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n)$

</details>

### Animal Shelter

#### An animal shelter, which holds only dogs and cats, operates on strictly 'first in, first out' basis. People must adopt either the 'oldest' (based on arrival time) of all the animals at the shelter, or they can select whether they would prefer a dog or cat (and will receive the oldest animal of that type). They cannot select which specific animal they would like. Create the data structures to maintain this system and implement operations such as enqueue, dequeue_any, dequeue_dog, and dequeue_cat.

<details>

  <summary>Solution</summary>

- Use Animal Parent class, Dog and Cat would inherit from it
- create two queues for dogs and cat

</details>
