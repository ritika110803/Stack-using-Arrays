C Program: Stack Implementation Using Array

This project demonstrates how to implement a *Stack Data Structure* using an array in C.

---

Description

The program:

* Implements a stack using a fixed-size array
* Performs basic stack operations:

  * *Push* (Insert element)
  * *Pop* (Remove element)
  * *Display* (Show stack elements)
* Handles *Stack Overflow* and *Stack Underflow* conditions

This example is ideal for beginners learning about *Stacks in Data Structures*.

---

Source Code

c

#include <stdio.h>

#include <stdlib.h>

#define MAX 5

int stack[MAX];

int top = -1;

// Push operation

void push(int value) {
   
    if (top == MAX - 1) {
        printf("Stack Overflow! Cannot push %d\n", value);
    } else {
        top++;
        stack[top] = value;
        printf("%d pushed into stack\n", value);
    }
}

// Pop operation

void pop() {
    
    if (top == -1) {
        printf("Stack Underflow! Cannot pop\n");
    } else {
        printf("%d popped from stack\n", stack[top]);
        top--;
    }
}

// Display stack

void display() {
    
    if (top == -1) {
        printf("Stack is empty\n");
    } else {
        printf("Stack elements are:\n");
        for (int i = top; i >= 0; i--) {
            printf("%d\n", stack[i]);
        }
    }
}

int main() {
   
    push(10);
    push(20);
    push(30);
    display();

    pop();
    display();

    return 0;
}


---

How to Compile and Run

Using GCC

1. Save the file as stack_array.c
2. Open terminal or command prompt
3. Compile the program:


gcc stack_array.c -o stack_array


4. Run the executable:


./stack_array


(On Windows, use stack_array.exe)

---

Sample Output


10 pushed into stack
20 pushed into stack
30 pushed into stack
Stack elements are:
30
20
10
30 popped from stack
Stack elements are:
20
10


---

Concepts Covered

* Stack Data Structure
* Array implementation of stack
* Push operation
* Pop operation
* Stack Overflow and Underflow
* LIFO (Last In, First Out) principle

---

How Stack Works

A stack follows the *LIFO (Last In, First Out)* principle:

* The last element inserted is the first one removed.
* top keeps track of the current top element.
* Initially, top = -1 (stack is empty).
* push() increments top.
* pop() decrements top.

---

Time Complexity

* *Push:* O(1)
* *Pop:* O(1)
* *Display:* O(n)

---

⚠️ Limitations

* Fixed size (MAX = 5)
* Cannot grow dynamically
* Uses global variables

---

Possible Improvements

* Implement stack using linked list
* Make it menu-driven
* Allow user input
* Add peek operation

---
