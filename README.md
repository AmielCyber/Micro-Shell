<h1 align="center">Unix Micro Shell Emulator</h1>

## Description
A C program that emulates a Unix Shell.

## File Manifest
* Makefile
* header.h 
* main.c 
* processes.c 
* shell.c 
* README.md 
* Shell Emulator Diagrams.pdf

## Compile and Start Program Instructions
* Enter the command `make` in the Unix terminal from this repository to compile the micro shell program.
* Enter the command `msh` to run the micro shell
* Enter the command `make clean` in the Unix terminal to remove the executable and any other generated files.
    * This will allow smooth recompilation with make

## Operating Instructions
* After running the program, type in the name or path of the file you'd like to run. 
* You may also pipe multiple files within the command line. 
* Entering the command `exit` will exit the program while running msh. 

## Design Decisions
We decided to split the program into 3 .c files and one header file. 
The 3 .c files, main.c, shell.c, and processes.c each handled a different part of the program. 
* **main.c** simply launches the program and calls the begin_shell function in shell.c. 
* **shell.c** handles all parts of the program associated with running the shell, managing user input, 
and ensuring graceful voluntary exit. It then passes on the parsed input to **processes.c**. 
* **processes.c** handles launching of the executable files or chaining the multiple executables to ensure a proper pipe, 
alongside any ungraceful exits. 
* **header.h** file is where we stored all of our included libraries, function prototypes, constants, and structures. 
An if-not-defined statement is included to ensure that nothing is added in to the compilation 
and pre-processing process more than once.

## Extra Features
Debugging tool function.

Followed good practice in .c, .h, and makefile files.

## Known Bugs
* `cd` works on some unix systems

## Lessons Learned
We learned how to, essentially, make a basic command line/shell. 
We were able to use system functions such as execvp, fork, 
and pipefd to properly launch (any number) applications and ensure a safe launch as well. 
Furthermore, my Amiel and I used git within this assignment. 

## Authors
* [Obada Algha](https://github.com/obadaalagha)
* [Amiel Nava](https://github.com/AmielCyber)
