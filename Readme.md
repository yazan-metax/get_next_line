# get_next_line() 👓📁

## introduction:)

- The get_next_line() function in C is a custom function often used for reading a file line by line. It's particularly handy when dealing with input from files of unknown or dynamic lengths. This function reads the file descriptor until a newline character ('\n') is encountered, allowing you to process the file content line by line.

- Its core functionality typically involves reading from a file or an input stream (like stdin) until it reaches a newline character or the end of the file. Upon encountering a newline character, it stores the line read into a buffer and returns it to the calling function. Subsequent calls to get_next_line() continue from where the previous call left off, allowing you to retrieve subsequent lines.

## Note 🚨: 
- Reading a line from a fd is way too tedious
## GOALS
This project will not only allow you to add a very convenient function to your collection, but it will also make you learn a highly interesting new concept in C programming: static variables.

## requirements ℹ️:

- ### ✏General Information about `open()`, `read()` Functions, and `File Descriptors`😎.

- ### open() Function:
```
- open() is a system call used to open files in C. It returns a file descriptor that uniquely identifies an open file in the operating system.
- Syntax:int open(const char *pathname, int flags);
- pathname: specifies the path to the file.
- flags: indicate the mode in which the file should be opened (e.g., read-only, write-only, read-write, etc.).
- file access modes can be specified using flags like O_RDONLY, O_WRONLY, O_RDWR, and other options like O_CREAT, O_APPEND, etc.
```
- ### read() Function:
```
- read(): is used to read data from an open file descriptor into a buffer.
- Syntax: ssize_t read(int fd, void *buf, size_t count);
- fd: is the file descriptor obtained from open().
- buf is the buffer where the read data will be stored.
- count is the number of bytes to read.
- Returns the number of bytes read or -1 on error.
```
- ### file Descriptor:
```
- A file descriptor is an integer value used to uniquely identify an open file in an operating system. It's an index into the file descriptor table maintained by the kernel.
- standard input (stdin), standard output (stdout), and standard error (stderr) are represented by file descriptors 0, 1, and 2, respectively.
- When a file is opened using open(), a new file descriptor is created.
- File descriptors are used by various I/O system calls (read(), write(), close(), etc.) to perform operations on files or other I/O resources.
```
### `static variable`:
- In C, a static variable is a type of variable that retains its value between function calls and has a different scope compared to regular variables.
- important key-points:
- ###  Lifetime and Scope:
- Lifetime: Static variables have a lifetime that spans the entire execution of the program. They are initialized only once before the program starts and retain their values throughout the program's execution.
- cope: The scope of a static variable is limited to the block in which it is declared, similar to local variables. However, static variables maintain their values across function calls within that scope.
- ### Initialization:
- By default, static variables are initialized to zero (0) if no explicit initialization is provided. For instance, `static int x;` will set x to 0.
- You can also explicitly initialize a static variable during declaration: `static int count = 0;`.
- ### Usage and Purpose:
- Persistence: They are commonly used when a variable's value needs to persist between function calls.
- Information Hiding: Static variables within functions help encapsulate data within that function and prevent external access, aiding in modular programming.
- ### Function Scope:
- Static variables inside functions are only accessible within that function. They are not visible or accessible from outside that function scope.

### example of the usage of static variables:
```
#include <stdio.h>

void exampleFunction() {
    static int count = 0; // Static variable declaration

    count++; // Increment count
    printf("Count is: %d\n", count);
}

int main() {
    exampleFunction(); // Outputs: Count is: 1
    exampleFunction(); // Outputs: Count is: 2
    exampleFunction(); // Outputs: Count is: 3

    return 0;
}
```
## usage⚙️:

### requirements:
- gcc compiler.
- c libraries(you can find them in the header files).
### Instructions
- to use this function in your code simply include the files inside your program then add the header into your header file or directly to your c file.
```
#include "get_next_line.h"
```
- this function can be compiled by adding the source files and the necessary flags.
```
gcc -Wall -Werror -Wextra -D BUFFER_SIZE=xx get_next_line.c get_next_line_utils.c && ./a.out
```
## final note 📍:
- İ included the main function for both mandatory and bonus part you can simply use them by commenting them in.
- İ also added test files(file.txt) ,you can change what is inside them upon your need.

# i hope you find this explanation useful for your need😃:)
