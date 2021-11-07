# CLI CheatSheet for BASH commands

##  [pwd](https://www.geeksforgeeks.org/xargs-command-unix)

xargs command is used to build and execute commands from standard input.it executes echo by default.
```
xargs [options] [command]

```
xargs with ls command-gives no.of works,lines,characters
```
ls *.txt | xargs wc
```
xargs with find command-delete temperory files
```
find /tmp -name "*.tmp" | xargs rm
```
xargs to read a file
```
xargs -a test.txt
```
xargs executing mkdir command
```
echo "f1 f2 f3" | xargs mkdir
```
limit output per line
```
echo "1 2 3 4 5 6 7 8 9" | xargs -n 3
```
xargs with grep
```
find -name "*.txt" | xargs grep "great"
```

##  [printenv command](https://www.sanfoundry.com/printenv-command-usage-examples-linux/)

it prints the values of the specified environment variables. If no variable is specified, print name and value pairs for them all.
```
printenv [OPTION] [VARIABLE]
```
```
options:
-0,--null
end each output line with 0 byte rather than newline
--help
display help and exit
```

printing all variable's name and value pairs
```
printenv
```
To get details of specified variable
```
printenv SHELL----->for 1 variable
printenv SHELL HOME----->for more than 1
```

##  [nano command](https://linuxize.com/post/how-to-use-nano-text-editor/)

Nano is a user-friendly, simple and WYSIWYG(What You See Is What You Get) text editor, which improves the features and user-friendliness of UW Pico text editor.

To create and open a new file.
```
nano new_filename
```
**nano shortcut keys**

To save a file
```
press Ctrl+o
```
To cut paste in a file
```
Ctrl+o is used to cut and Ctrl+u is used to paste the text.
```
To search a word in a file.
```
press Ctrl+w
```
To do spell check 
```
press Ctrl+t
```

##  [Pipe operator](https://www.geeksforgeeks.org/piping-in-unix-or-linux/)

A pipe is a form of redirection to send the output of one command to another command for further processing and it combines two or more commands.
Pipes are unidirectional i.e **data flows from left to right through the pipeline.**

```
command_1 | command_2 | command_3 | .... | command_N 
```
Listing all files and directories and give it as input to more command.
```
ls -l | more 
```
Use sort and uniq command to sort a file and print unique values.
```
sort record.txt | uniq 
```
Use head and tail to print lines in a particular range in a file.
```
cat sample2.txt | head -7 | tail -5
```
Use cat, grep, tee and wc command to read the particular entry from user and store in a file and print line count.
```
cat aaaa | grep "apple" | tee file2.txt | wc -l
```
