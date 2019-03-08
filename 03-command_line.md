# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

* **pwd** - show current working directory path
* **mkdir** - creating a directory
* **rmdir** - deleting a directory (empty)
* **rm -rf** - deleting a directory (non empty)
* **touch** - creating a file using `touch` command
* **rm** - deleting a file
* **mv file1 file2** - renaming a file from file1 to file2
* **ls .?\*** - listing hidden files
* **cp SOURCE DESTINATION** - copying a file from one directory (SOURCE) to another (DESTINATION)
* **diff file1 file2** - looks at file1 and file2 and shows the difference 
---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

ls - displays all files
ls -a - displays all files (including hidden files)
ls -l - displays files in long listing
ls -lh - displays files in long listing, with unit suffixes
ls -lah - displays all files in long listing, with unit suffixes
ls -t - displays files by newest first
ls -Glp - displays files in long list, directories highlighted in color with ending in / 
---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

ls -R: displays subdirectories
ls -p: displays directories with /
ls -r: displays in reverse order
ls -S: displays by size (largest first)
ls -u: displays files by access time

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

xargs can take a stream of input and use it as an argument of another command (just echos if there is no follow up command)

For example: the following bash command prints out a list of all files in a single line (since no command follows args):

'''console
$ ls -l | xargs
'''
 

