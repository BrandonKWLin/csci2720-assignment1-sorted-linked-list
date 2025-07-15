⚠️ **DISCLAIMER:** Do NOT copy or submit this project as your official assignment. Doing so is an academic violation and may result in disciplinary action. This README is provided for learning and personal reference only.
⚠️ This is for employment purposes, to be included in the projects section of my resume.
# CSCI 2720 - Assignment 1

**Name:** Brandon Lin

---

## Overview

This project is a Java-based command-line application implementing a sorted singly linked list. It supports operations like insertion, deletion, searching, merging, deleting alternate nodes, and finding the intersection of two lists. The application reads input from a text file and offers an interactive interface for users to manage list operations.

---

## Compiling

Navigate to the assignment directory:

```bash
cd ~/csci2720/assignments/Lin_assignment1
```

Compile all Java source files into the `bin` directory:

```bash
javac -d bin src/*.java
```

---

## Running

Run the program using:

```bash
java -cp bin LinkedListDriver input.txt
```

---

## Pseudocode for Merge Function

- Create a new `SortedLinkedList` to store the merged result.
- Set `firstCurr` and `secondCurr` to the heads of the two input lists.
- While both pointers are not null:
  - If `firstCurr.info` < `secondCurr.info`, insert `firstCurr.info` into the new list and advance `firstCurr`.
  - If `firstCurr.info` > `secondCurr.info`, insert `secondCurr.info` into the new list and advance `secondCurr`.
  - If values are equal:
    - Insert one value into the new list.
    - Advance both pointers.
- Once one list is exhausted, insert any remaining elements from the other list into the new list.
- Update the original list’s head to `mergedList.head`.
- Print the merged list.

**Time Complexity:**  
- Main comparison loop runs in O(n + m).
- Each `insertItem` is O(n + m), so inserting all (n + m) items yields O((n + m)²).
- Updating the head is O(1).
- Printing the list is O(n + m).
- **Total time complexity:** O((n + m)²).

---

## Pseudocode for Intersection Function

- Create a new `SortedLinkedList` called `newList`.
- Set pointers `first` and `second` to the heads of the two input lists.
- While both pointers are not null:
  - If `first.info` < `second.info`, move `first` forward.
  - If `first.info` > `second.info`, move `second` forward.
  - If values are equal:
    - Insert the value into `newList`.
    - Advance both pointers.
- Iterate through `newList` to print its elements.

**Time Complexity:**  
- Each node in both lists is visited at most once.
- **Total time complexity:** O(n + m).

---
