# Shell scripts library
Shlib is a library to easily manage own shell scripts from terminal in Linux. Imported scripts can be immediately used as traditional commands.

## Example
This is an example of shell script called `helloworld` stored in `~/`
```Shell
#!/bin/sh
echo "Hello world!"
```
Adding this script to the library, it is used as a command
```ShellSession
[guest@github ~]$ shlib -a helloworld
[guest@github ~]$ helloworld
Hello World!
```
Print all scripts in the library
```ShellSession
[guest@github ~]$ shlib -l
anonimize	createtxt	helloworld	tarandrm
```

## Installation
To install shlib, navigate with `cd` command into downloaded repo folder and run installation script with `./initshlib`.

## Manual
```
Usage:
	shlib [-l] [-E] [-a -o script] [-n -o script] [-e script] [-r script...] [-I -o archive]
Description:
	shlib manages personal shell scripts. Scripts can be used as traditional command terminal.
Option:
	-a | all	Add an existing script to the library. The name of th file should be extensionless
			and it will be the name of the command.
	-n | new	Add a new script to the library and automaticaly open vim to edit its.
	-e | edit	Edit an existing script of the library.
	-l | list	Print the list of all library's scripts.
	-r | remove	Remove a script or a list of scripts from the library.
	-E | export	Export all library's scripts saving them in a compressed archive.
	-I | import	Import all scripts in a compressed archive.
	-o		Adding this options to some other, force to overwrite any existing script with
			the same name.
```

## Troubleshooting
* Portability has still not been tested. It works on Fedora 23

## Feeds
* Bug report: [Open an issue](https://github.com/matteocellucci/shlib/issues/new)
* Feature request: [Open an issue](https://github.com/matteocellucci/shlib/issues/new)

## Changelog
* 2015 December 10, 1.1.2
	- Add long version options in the manual
* 2015 November 29, 1.1.1
	- Implement functionaly to remove more then one script `shlib -r script...`
	- Fix some minor issues
* 2015 November 28, 1.0.0
	- Birth

## License
This project is released under [The MIT Licenese (MIT)](https://github.com/matteocellucci/shlib/blob/master/license).
