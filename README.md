# Run C

Sometimes you do not want to use an IDE but you want to work on some C code, for example: when working over ssh.
This bash utility will allow you to run code as such:

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
