# get_next_line() 👓📁

## introduction:)

- The get_next_line() function in C is a custom function often used for reading a file line by line. It's particularly handy when dealing with input from files of unknown or dynamic lengths. This function reads the file descriptor until a newline character ('\n') is encountered, allowing you to process the file content line by line.

- Its core functionality typically involves reading from a file or an input stream (like stdin) until it reaches a newline character or the end of the file. Upon encountering a newline character, it stores the line read into a buffer and returns it to the calling function. Subsequent calls to get_next_line() continue from where the previous call left off, allowing you to retrieve subsequent lines.

## GOALS
This project will not only allow you to add a very convenient function to your collection, but it will also make you learn a highly interesting new concept in C programming: static variables.

## requirements ℹ️:

- ### ✏️General Information about `open()`, `read()` Functions, and `File Descriptors`.

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



