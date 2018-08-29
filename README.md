# 0x15. C - Simple Shell
---
## Name

Shell - A simple shell

## Description

This project recreates a simple command line shell that executes commands read from the standard input or from a file. 

* Can execute any commands from the environment path.
* Works on interactive and non-interactive mode.
* Commands must be on a single line.
* Arguments must be separated by whitespace.
* No quoting arguments and escaping whitespace.
* No piping or redirection.
* It doesn't handle aliases, comments or  history.
* Built-in commands:

  - env (print a list of the current environment variables).

  - exit (exits the shell).

##### Example 1 | cat command

```
$ cat environ.c
#include "shell.h"

/**
 * print_env - a function that prints the environment.
 * Return: 0.
 */

int print_env(void)
{
	int i = 0;

	while (environ[i])
	{
		/* prints in form of "variable=value" */
		   write(1, environ[i], _strlen(environ[i]));
		   	    i++;
				write(1, "\n", 1);
				}
				return (0);
}

$

```

##### Example 2 | BUILT-IN COMMAND: exit

```

vagrant@simple_shell$ ./hsh
$ echo Quitting the simple shell with the exit command
Quitting the simple shell with the exit command
$ exit
vagrant@simple_shell$

```

### List of allowed functions and system calls
* access (man 2 access)
* chdir (man 2 chdir)
* close (man 2 close)
* closedir (man 3 closedir)
* execve (man 2 execve)
* exit (man 3 exit)
* fork (man 2 fork)
* free (man 3 free)
* stat (__xstat) (man 2 stat)
* lstat (__lxstat) (man 2 lstat)
* fstat (__fxstat) (man 2 fstat)
* getcwd (man 3 getcwd)
* getline (man 3 getline)
* kill (man 2 kill)
* malloc (man 3 malloc)
* open (man 2 open)
* opendir (man 3 opendir)
* perror (man 3 perror)
* read (man 2 read)
* readdir (man 3 readdir)
* signal (man 2 signal)
* strtok (man 3 strtok)
* wait (man 2 wait)
* waitpid (man 2 waitpid)
* wait3 (man 2 wait3)
* wait4 (man 2 wait4)
* write (man 2 write)
* _exit (man 2 _exit)
* isatty (man 3 isatty)
* fflush (man 3 fflush)

---
File|Task
---|---
man_1_simple_shell | manual page
_getenv.c | gets an environment variable
_strlen.c | returns the length of a string
_which.c | checks wether a file exists in the PATH
compstr.c | compares two strings
environ.c | prints the environment
few.c | creates and executes a process
path.c | handles the PATH
pid.c | get process ID of the calling process
ppid.c | return the process ID of the parent process
shell.c | the main componenets of the shell
shell.h | the header file for the simple shell program
str_concat.c | concatenates two strings
strdup.c | duplicates a string
tokenize.c | splits a string into tokens
toksize.c | count the number of tokens

#### Compilation

Files are compiled this way:

$ gcc -Wall -Werror -Wextra -pedantic *.c

### Authors

[Francesca Cantor](https://github.com/fcantor)

[Leine Valente](https://github.com/leinefran)

[Nicole Swanson](https://github.com/thenicopixie)