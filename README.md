# Run C

When testing C code on a shell I often find myself repeating the steps of re-compiling and re-running an executable as I debug a program. The process can be tedious when repeated dozens of times in a row. 

This utility allows you to compile and run your C code in one line. Additionally, no executable will be left behind so there's no need to worry about file clutter.

The utility is invoked as such:

```
runc someFile.c
```

## How it works
The following steps will be taken:
  1. Checks for GCC installation
  2. Compiles the source code into an executable
  3. Runs the executable
  4. Deletes the executable
  
## Installation

You can use the 'runc' shell script directly from a directory or install it to a foder in your PATH variable to access it from any directory. The following instructions will place the script in an OS friendly directory.

Instructions assume the working directory contains the 'runc' file.

### MacOS
```
cp runc /usr/local/bin/runc
```
### Linux
```
cp runc /usr/bin/runc
```

## Time Measurement

As of 1.1 it is possible to output the time it took for the program to compile as well as the time it took to execute. This can be triggered by appending the [-t] flag to the call as such:

```
runc someFile.c -t
```

Your output will be formatted as such:

```
real    0m0.088s
user    0m0.049s
sys     0m0.030s
"Hello World"
real    0m0.005s
user    0m0.001s
sys     0m0.002s
```

In the above example the program took 0.088 seconds to compile and 0.005 seconds to execute. The program outputted "Helo World".

'user', or User time is the amount of CPU time spent in user-mode code (outside the kernel) within the process.

'sys', or System time is the amount of CPU time spent in the kernel within the process.

Future releases will aim to format this in a more human-friendly way.