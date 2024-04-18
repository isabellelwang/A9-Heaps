# Heaps of Fun

For this project, you'll be creating a new class called `Heap` using an `ArrayList` for base storage. Some methods are provided for you in `Heap.java`. You'll need to fill in the definitions for the rest. When you are done, you'll write a short test program to try everything out.

## Phase One: Implementation

Some of the method definitions in `Heap.java` have been left empty. Your job is to fill in the implementations. The comments in the function headers tell you what each method should do and sometimes give you some hints to help guide your approach.

First implement the methods `parent`, `leftChild`, and `rightChild`. You can find some helpful equations for this in slide deck 27.

Next, implement `insert` and `popTop` to add and remove elements from the heap.

Test your implementation using a `HeapTest` class.  At minimum, you should make sure the following work as expected:
* Create a heap `h` and insert 10 or so random numbers (ideally they should not be in order). Print out the heap after each insertion so you can check that it is developing properly.
* Pop a few elements off the heap.  Make sure that you are getting the largest remaining value each time and that the heap structure is updated properly after the root is removed.

## Phase Two: Heap Sort

For the second part of the project, you will implement heap sort. To do this, you should start by implementing the `bubbleUp` and `bubbleDown` methods defined in class `Heap`.

Since the `heapSort` method is takes an `ArrayList` of elements, you should build a temporary `Heap` object around the existing list.  Because your `Heap` class uses an `ArrayList` for its back-end implementation, you can do this by defining a private constructor that takes the `ArrayList` that needs to be sorted as an argument.  Once you've done this, you can use the existing `Heap` methods to sort the elements.  At the end, return the original `ArrayList`, whose elements will now be sorted.

When testing, you may find it useful to use the following syntax to create and initialize your array:

    Integer arr[] = {-2,3,9,-7,1,2,6,-3};
    ArrayList<Integer> al = new ArrayList<>(Arrays.asList(arr));
    // Call your heap constructor with `al` passed as an argument
    // Use heap methods to sort the heap
    // Set `al` equal to the ArrayList stored in the heap with heap.getData()