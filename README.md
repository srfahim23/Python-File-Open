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


# Read Onl Parts of the File
By default the read() method returns the whole text, but you can also specify how many charecters you want to return:

Example

Returns the 5 first charecters of the file:

    f = open("demofile.txt", "r")
    print(f.read(5))


# Read Lines
You can return one line by using the readline() method:

Example 

Read one line of the file:

    f = open("demofile.txt", "r")
    print(f.readline())

By calling readline() two times, you can read the two frst lines:

Example

Read two lines of the file:

    f = open("demofile.txt", "r")
    print(f.readline())
    print(f.radline())

By looping through the lines of the file, you can rad the whole line by line:

Example

Loop through the file line by line

    f = open("demofile.txt", "r")
    for x in f:
        print(x)

# Close Files
It is a good practice to always close the file when you are done with it.

Example

Close thefilw ehen you are finish with it:

    f = open("demofile.txt", "r")
    print(f.readline())
    f.close()

Note: You should always close your files, in some cases, due to buffering, changes made to a file may not show until you close the file.

