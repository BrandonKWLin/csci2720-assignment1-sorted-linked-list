CSCI 2720 - Assignment 1
Name 1: Brandon Lin



Compiling:

Navigate to the directory ~/csci2720/assignments/Lin_assignment1 by entering:
cd ~/csci2720/assignments/Lin_assignment1

Compile the Java source files into the bin directory:
javac -d bin src/*.java

Running:
Use the following command to execute the program:
java -cp bin LinkedListDriver input.txt

Pseudocode for merge function:
Start by creating a new SortedLinkedList that will hold the combined result of the merge. Set two pointers, firstCurr and secondCurr, to the heads of the two input lists. While both pointers are not null, compare the values they point to. If firstCurr.info is less than secondCurr.info, insert that value into the new list and move firstCurr forward. If it’s greater, insert the value from secondCurr and move that pointer forward. If the two values are equal, insert one of them into the new list and advance both pointers. After the main loop ends, add any remaining nodes from either list into the merged list. Finally, update the original list’s head to point to mergedList.head and print out the final list.

Time complexity: The main comparison loop runs in O(n + m) where n and m are the sizes of the two lists. Each insertItem operation is O(n + m), and since you insert n + m items total, the insertions together cost O((n + m)²). Updating the head is O(1), and printing the list is O(n + m). Therefore, the total time complexity of the mergeLists function is O((n + m)²).

Pseudocode for intersection function:
Begin by initializing a new SortedLinkedList called newList to store the common elements. Set two pointers, first and second, to the heads of the two lists. While neither pointer is null, compare their current values. If first.info is less than second.info, move first forward. If it’s greater, move second forward. When the values are equal, insert that value into newList and advance both pointers. Once done, use a third pointer current to iterate through newList and print each value.

Time complexity: Each node in both lists is visited at most once, resulting in a time complexity of O(n + m), where n and m are the lengths of the two input lists.

