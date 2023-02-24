# Python-File-Open
File handling is an important part of any web application.

Python has several functions for creating, reading, updating, and deleting files.

# File Handling
The key function for working with files in Python is the open() function.

The open() funciton takes two parameters; filename, and mode.

There are four different methods (modes) for opening a file:

"r" - Read - Default value. Opens a file for raeding, error if the file does not exit

"a" - Appent - Opens a file for appending, creates the file if it does not exit

"w" - Write - Opens a file for writing, creates the file if it does not exit

"x" - Create - Creates the specified file, returns an error if the file exists

In addition you can specify if the file shuld be handled as binary or text mode

"t" - Text - Default value. Text mode

"b" - Binary mode (e.g. images)


# Syntax
To open a file for reading it is enough to specify the name of the file:

     f = open("demofile.txt")

The code above is the same as:

    f = open("demofile.txt", "rt")

Because "r" for read, and "t" for text are the default values, you do not need to specify them.

Note: Make sure the file exitst or else you will get an error.

# Python File Open
# Open a File on the Server
Assume we have the following file, located in the same folder as Python:

demofile.txt

    Hello! Welcome to demofile.txt
    This file is for testing purposes.
    Good Luck!


To open the file, use the built-in open() function

The open() function returns a file object, which has a read() method for reading the content of the file:

Example:

    f = open("demofile.txt", "r")
    print(f.read())

If the file is located in a different location, you will have to specify the file path, like this:

Example

Open a file on a different location:


    f = open("D:\\myfiles\welcome.txt", "r") 
    print(f.read())
