# Shell scripts library
Shlib is a library to easily manage own shell scripts from terminal in Linux. Imported scripts can be immediately used as traditional command.

## Example
```Shell
#!/bin/sh
# This is mynewscript
echo "Hello World!"
```
```ShellSession
[guest@github ~]$ shlib -a mynewscript
[guest@github ~]$ mynewscript
Hello World!
[guest@github ~]$ shlib -l
mynewscript	myoldscript	anotherscript
[guest@github ~]$
```

## Installation
To install shlib, navigate with `cd` command into downloaded repo folder and run installation script with `sudo ./initshlib`.

## Manual
Usage:
	shlib [-l] [-a -o script] [-n -o script] [-e script] [-r script] [-I -o archive] [-E archive]
Description:
	shlib manages personal shell scripts. Scripts can be used as traditional command terminal.
Option:
	-a	Add an existing script to the library. The name of th file should be extensionless and it will be the name of the command
	-n	Add a new script to the library and automaticaly open vim to edit its
	-e	Edit an existing script of the library
	-l	Print the list of all library's scripts
	-r	Remove a script from the library	
	-E	Export all library's scripts saving them in a compressed archive
	-I	Import all scripts in a compressed archive
	-o	Adding this options to some other, force to overwrite any existing script with the same name

## Troubleshooting
* Portability has still not been tested. It works on Fedora 23.

## License
This project is released under The MIT Licenese (MIT). You can find a copy [here](https://github.com/matteocellucci/shlib/blob/master/license).
