# Student Record Management System

A **console-based Student Record Management System developed in C** using **structures, linked lists, dynamic memory allocation, and file handling**.

The project is designed to manage student records efficiently through a menu-driven interface. Student data can be added, viewed, searched, modified, deleted, and stored in a file for persistent use.

## Features

* Add new student records
* View all student records
* Search student records
* Modify existing student details
* Delete student records
* Sort student records
* Store student records in a file
* Load previously stored records when the program starts
* Generate unique roll numbers
* Dynamic memory allocation using linked lists
* Menu-driven console interface

## Student Information

Each student record contains:

* Roll Number
* Student Name
* Marks

## Technologies Used

| Technology                | Purpose                           |
| ------------------------- | --------------------------------- |
| C                         | Programming language              |
| GCC                       | Compilation                       |
| Linked List               | Dynamic student record management |
| Structures                | Student data organization         |
| Dynamic Memory Allocation | Runtime memory management         |
| File Handling             | Permanent data storage            |
| Git                       | Version control                   |
| GitHub                    | Source code hosting               |

## Data Structure

The project uses a **singly linked list** to store student records dynamically.

Each node contains:

```c
typedef struct student
{
    int roll;
    char name[20];
    float marks;
    struct student *next;
} ST;
```

The `next` pointer connects one student record to the next record.

### Linked List Representation

```text
+---------+----------+-------+------+
| Roll No |   Name   | Marks | Next |
+---------+----------+-------+------+
                    |
                    v
              +---------+----------+-------+------+
              | Roll No |   Name   | Marks | Next |
              +---------+----------+-------+------+
                                             |
                                             v
                                            NULL
```

## File Handling

The system uses file handling to preserve student records between program executions.

The program:

1. Opens the student data file when the program starts.
2. Reads previously stored records.
3. Creates linked-list nodes dynamically.
4. Loads the records into memory.
5. Allows the user to perform operations.
6. Stores the updated records back into the file.

This allows student data to remain available even after the program is closed.

## Roll Number Generation

The system generates roll numbers based on the student's name.

The first letter of the student's name is converted to uppercase and used to generate a sequential number.

Example:

```text
Akash   → A1
Arun    → A2
Bala    → B1
Bharath → B2
```

This avoids duplicate numbering for students beginning with the same letter.

## Project Structure

```text
STUDENT-RECORD-MANAGEMENT-SYSTEM/
│
├── finalissuesfixedstudentprojectfinalout/
│   ├── source files
│   ├── header files
│   ├── data file
│   └── other project files
│
└── README.md
```

## Concepts Demonstrated

This project demonstrates practical implementation of several C programming concepts:

* Structures
* Pointers
* Pointer to structure
* Singly linked lists
* Dynamic memory allocation
* `malloc()` and `free()`
* Functions
* File handling
* `fopen()`
* `fscanf()`
* `fprintf()`
* `rewind()`
* String handling
* Conditional statements
* Loops
* Menu-driven programming
* Modular programming using header files

## Compilation

If the project contains multiple C source files, compile them using GCC:

```bash
gcc *.c -o student
```

Run the program:

```bash
./student
```

Alternatively, compile individual source files:

```bash
gcc -c main.c
gcc -c add.c
gcc -c delete.c
gcc -c search.c
```

Then link the object files:

```bash
gcc *.o -o student
```

## Example Menu

```text
====================================
     STUDENT RECORD MANAGEMENT
====================================

A : Add Student
D : Delete Student
S : Search Student
M : Modify Student
V : View Students
T : Sort Students
E : Exit

====================================
Enter your choice:
```

## Learning Outcome

This project helped in understanding how **C programming concepts can be combined to build a practical application**.

It provides hands-on experience with:

* Dynamic data structures
* Memory management
* File-based persistence
* Modular C programming
* Pointers and structures
* Debugging and compilation using GCC
* Version control using Git and GitHub

## Author

**Akash S**

Electrical and Electronics Engineering Graduate
Embedded Systems / C Programming Enthusiast

## Repository

Source code is available on GitHub:

[STUDENT-RECORD-MANAGEMENT-SYSTEM](https://github.com/Akash-1414/STUDENT-RECORD-MANAGEMENT-SYSTEM?utm_source=chatgpt.com)
