# Run C

When testing C code on a shell I often find myself repeating the steps of re-compiling and re-running an executable as I debug a program. The process can be tedious when repeated dozens of times in a row. 

This utility allows you to compile and run you C code in one line. Additionally, no executable will be left behind so there's no need to worry about file clutter.

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

### MacOS
```
cp runc /usr/local/bin/runc
```
### Linux
```
cp runc /usr/bin/runc
```
