# Git Bash Homework 1 
## 1. __Check where am I:__


``` pwd ``` - the command allows us to check the current directory.
``` 
 ~/lentochka_7   pwd                                                                                                                   
/home/lentochka_7
```
## 2. Make a new folder:
```mkdir```- allows us to create a new folder (directory) 
```
~/lentochka_7  
mkdir Homework  
```
## 3. Go to the created folder:
``` cd```- allows us to go to any folder (directory)
```
 ~/lentochka_7 
  cd Homework                                                                                                           
 ~/lentochka_7/Homework 
```
## 4. Make 3 new folders:
With command ```mkdir``` we can create a multiple directories (folders).
We need to type the names of new directories separated by space.
```
~/lentochka_7/Homework 
 mkdir terminal1 terminal2 terminal3
```
## 5. Go to any of these 3 folders:
We also use ```cd``` command.
```
~/lentochka_7/Homework  
cd terminal3                                                                                               
~/lentochka_7/Homework/terminal3 
```
## 6. Create 5 files (3.txt, 2.json):
If we create empty files, we use ```touch``` command. Take files in quates and write with 
a space.
```
~/lentochka_7/Homework/terminal3  
touch "pwd.txt" "ls.txt" "cd.txt" "cat.json" "tail.json"                                           
```
## 7. Make 3 new folders:
Using ```mkdir``` here agan.
```
~/lentochka_7/Homework/terminal3  mkdir git_1 git_2 git_3 
```
## 8. Show the list of current folder elements:
```ls```- command show the content of a folder.
Also we can using:

```
~/lentochka_7/Homework/terminal3  
ls                                                                                                 
cat.json  cd.txt  git_1  git_2  git_3  ls.txt  pwd.txt  tail.json
```
## 9. Open one of txt files:
We usiing ```cat``` command
```
/lentochka_7/Homework/terminal3 
 cat ls.txt  
```
## 10. Write any thing in this file:
If we want to open file for editing, we can use ```cat>``` command, if the file is empty.
If we want to add something to the file which is not empty, we use ```cat >>```
```
~/lentochka_7/Homework/terminal3  
cat>ls.txt                                                                                     
Success does not consist in never making mistakes but in never
 making the same one a second time.  
^C 
```
## 11. Save and quite:
In order to save and exit editing, use the keyboard shortcut ```Ctrl + C```
## 12. Go to the directory located 1 level above:
If we want to go  1 level above, we are  to use command ```cd``` with ```..```
```
~/lentochka_7/Homework/terminal3  
cd ..                                                                                  
~/lentochka_7/Homework 
```
## 13. Move to any 2 files to any folder:
If we want to move any files from folder1 to folder2, we use ```mv -t``` command
```
~/lentochka_7/Homework  
mv -t terminal1 terminal3/pwd.txt terminal3/ls.txt 
```
## 14. Copy any 2 files to any folder:
The ```cp``` command can copy one or more files (directories) to another directory
```
/lentochka_7/Homework  
cp terminal3/{cat.json,tail.json} terminal2 
```
## 15. Find a file by name:
If we want to find file by name, we are to use ``` find -name```
```
~/lentochka_7  
find -name pwd.txt                                                                                                    
./Homework/terminal1/pwd.txt
```
## 16. Show file content in real time, 
To view the contents of new lines in a file in real time, use ```tail``` command with the 
```-f``` option added. Also, we can ```tail``` with ```grep```
```
~/lentochka_7/Homework/terminal3 
tail -f ls.txt 
```
## 17. Show several of the first lines from the text file:
```tail``` command can show us the first lines
```
~/lentochka_7/Homework/terminal3 
head -n 5 ls.txt                                                                                   
q1
q2
q3
q4
q5
```

## 18. Show several of the last lines from the text file:
```tail``` command can show us the last lines
```
~/lentochka_7/Homework/terminal3  
tail -n3 ls.txt                                                                                    
q7
q8
q9
```

## 19. Show several content of a large file:
```less``` alows us to rewind the text not only forward, but also backward, search in both
directions, jump immediately to the end or to the beginning of the file
```
~/lentochka_7/Homework/terminal3  
less ls.txt  
```
```q``` for exit

## 20. Show current date and time:
```date``` command show us current date and time
```
/lentochka_7/Homework/terminal3  
date                                                                                       
Tue May 16 09:02:12 AM +03 2023
```
## 21*. Additional tasks:
- Send an http request to the server http://162.55.220.72:5005/terminal-hw-request
  ```curl``` is a utility for transferring data from or to a server, designed to work without
user interaction.
```
 ~/lentochka_7/Homework/terminal3  
curl http://162.55.220.72:5005/terminal-hw-request                                                 
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<title>404 Not Found</title>
<h1>Not Found</h1>
<p>The requested URL was not found on the server. 
If you entered the URL manually please check your spelling and
try again.</p>
```







