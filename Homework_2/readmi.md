# Homework 2 
## 1. Make a folder named dir_1:
## ```mkdir dir_1 ```
## 2. Go to the folder dir_1:
## ```cd dir_1 ```
## 3. Create a folder named inner_dir_1:
## ```mkdir inner_dir_1 ```
## 4. Check where you are:
## ```pwd```
## 5. While located inside the dir_1 folder, create an empty text file named tf_1.txt:
## ```touch tf_1.txt```
## 6. While located the dir_1 folder, create a text file named tf_2.txt using the command cat with the following lines:
* ### the first 1
* ### the second 2
* ### the third 3
``` 
~/lentochka_7/homework_2/dir_1 
cat>tf_2.txt                                                                                        
the first 1
the second 2
the third 3
^C
```
## 7. Go to the folder inner_dir_1:
## ```cd inner_dir_1 ```
## 8.  Use the cat command to create a text file named tf_3.txt with any lines:
```
~/lentochka_7/homework_2/dir_1/inner_dir_1  
cat>tf_3.txt                                                                          
WHAT TESTING IS AND WHERE IT CAME FROM
WHO IS A TESTER AND WHAT IS THEIR WORK
WHAT YOU NEED TO KNOW AND BE ABLE TO LEARN
MYTHS AND MISCONCEPTIONS ABOUT TESTING
Software development models
Software testing lifecycle
Software testing principles
^C
```
## 9. Use the cat command to add the line "the second 2" to the text file tf_3.txt:
```
~/lentochka_7/homework_2/dir_1/inner_dir_1  
cat>>tf_3.txt                                                             
the second 2
^C
```
## 10. Use the cat command to add the line "the sec 2" to the text file tf_3.txt:
```
~/lentochka_7/homework_2/dir_1/inner_dir_1  
cat>>tf_3.txt                                                                
the sec 2
^C
```
## 11. Use the cat command to add the line "the sec 3" to the text file tf_2.txt:
```
 ~/lentochka_7/homework_2/dir_1/inner_dir_1  
cat> ../tf_2.txt                                                             
the sec 3 
^C
```
## 12. Use the cat command to add the line “the SeCoNd 2” to the text file tf_3.txt:
```
~/lentochka_7/homework_2/dir_1/inner_dir_1  
cat>>tf_3.txt                                                                
the SeCoNd 2
^C
```
## 13.Use the cat command to add the line “the SeCoNd 2” to the text file tf_2.txt:
```
~/lentochka_7/homework_2/dir_1/inner_dir_1  
cat>>../tf_2.txt                                                             
the SeCoNd 2
^C
```
## 14. Create a text file named tf_4.txt with 15 lines:
 ```
~/lentochka_7/homework_2/dir_1  
seq 1 15 | cat>inner_dir_1/tf_4.txt  
```
## 15. Create a text file named tF_5.txt  with 13 lines:
```
~/lentochka_7/homework_2/dir_1 
 seq 1 13 | cat>inner_dir_1/tF_5.txt 
```
## 16. Show a list of all files in the folder:
```
~/lentochka_7/homework_2/dir_1/inner_dir_1 
ls                                                                                      
tf_3.txt  tf_4.txt  tF_5.txt
```
## 17. Go out of the inner_dir_1 folder:
```
~/lentochka_7/homework_2/dir_1/inner_dir_1  
cd ..                                                                                  
~/lentochka_7/homework_2/dir_1 
```
## 18. Display the contents of the file tf_3.txt in the terminal:
```
~/lentochka_7/homework_2/dir_1  
cat inner_dir_1/tf_3.txt  
                                                                       
WHAT TESTING IS AND WHERE IT CAME FROM
WHO IS A TESTER AND WHAT IS THEIR WORK
WHAT YOU NEED TO KNOW AND BE ABLE TO LEARN
MYTHS AND MISCONCEPTIONS ABOUT TESTING
Software development models
Software testing lifecycle
Software testing principles
the second 2
the sec 2
the SeCoNd 2
```
## 19. Find the path to the file tf_4.txt:
```
~/lentochka_7/homework_2/dir_1 
find . -name "tf_4.txt"                                                                            
./inner_dir_1/tf_4.txt
```
## 20. Clear the contents of the file tf_4.txt without deleting the file itself:
```
/lentochka_7/homework_2/dir_1  
cat /dev/null >inner_dir_1/tf_4.txt 
```
OR
```
~/lentochka_7/homework_2/dir_1 
echo>inner_dir_1/tf_4.txt
```
## 21. Find the paths to files that have "tf" in their name:
```
~/lentochka_7/homework_2/dir_1 
find . -name "tf*.txt"                                                                              
./tf_1.txt

./inner_dir_1/tf_3.txt
./inner_dir_1/tf_4.txt
./tf_2.txt
```
## 22. ind the paths to files that have "tf" in their name with letters in any case:
```
~/lentochka_7/homework_2/dir_1 
find . -iname "tf*.txt" 
                                                                         
./tf_1.txt
./inner_dir_1/tf_3.txt
./inner_dir_1/tf_4.txt
./inner_dir_1/tF_5.txt
./tf_2.txt
```
## 23. Find lines in files that contain the letter combination "sec" in the current folder:
```
~/lentochka_7/homework_2/dir_1 
grep sec *.*   
                                                                                     
tf_2.txt:the sec 3 
```
## 24. Find lines in files that contain the letter combination "sec" in any case in the current folder:
```
~/lentochka_7/homework_2/dir_1 
grep -i sec *.*     
                                                                               
tf_2.txt:the sec 3 
tf_2.txt:the SeCoNd 2
```
## 25. Find lines in files that contain only the "sec" letter combination in the current folder:
```
~/lentochka_7/homework_2/dir_1 
grep -w sec *.*    
                                                                            
tf_2.txt:the sec 3
```
## 26. Find lines in files that contain only the "sec" letter combination in any case in the current folder:
```
~/lentochka_7/homework_2/dir_1 
grep -wi sec *.* 
                                                                                  
tf_2.txt:the sec 3 
```
## 27. Find lines in files that contain the letter combination "second" in the current folder:
```
~/lentochka_7/homework_2/dir_1 
grep -r second ./  
                                                                              
./inner_dir_1/tf_3.txt:the second 2
```
## 28. Find lines in files that contain the letter combination "second" in any case in the current folder:
```
~/lentochka_7/homework_2/dir_1 
grep -ri second ./                                                                                 

./inner_dir_1/tf_3.txt:the second 2
./inner_dir_1/tf_3.txt:the SeCoNd 2
./inner_dir_1/tf_2.txt:the SeCoNd 2
```
## 29. Find lines in files that contain the letter combination "second" in all subfolders:
```
~/lentochka_7/homework_2/dir_1 
grep -r second ././ 
                                                                             
././inner_dir_1/tf_3.txt:the second 2
```
## 30. Find only the path and file name in lines that contain the letter combination "second" in the current folder:
```
~/lentochka_7/homework_2/dir_1 
grep -rl second ./*                                                                              
./inner_dir_1/tf_3.txt
```
## 31. Find all lines in all files that do not contain the combination "second":
```
~/lentochka_7/homework_2/dir_1 
grep -rv "second"

inner_dir_1/tf_3.txt:WHAT TESTING IS AND WHERE IT CAME FROM
inner_dir_1/tf_3.txt:WHO IS A TESTER AND WHAT IS THEIR WORK
inner_dir_1/tf_3.txt:WHAT YOU NEED TO KNOW AND BE ABLE TO LEARN
inner_dir_1/tf_3.txt:MYTHS AND MISCONCEPTIONS ABOUT TESTING
inner_dir_1/tf_3.txt:Software development models
inner_dir_1/tf_3.txt:Software testing lifecycle
inner_dir_1/tf_3.txt:Software testing principles
inner_dir_1/tf_3.txt:the sec 2
inner_dir_1/tf_3.txt:the SeCoNd 2
inner_dir_1/tF_5.txt:1
inner_dir_1/tF_5.txt:2
inner_dir_1/tF_5.txt:3
inner_dir_1/tF_5.txt:4
inner_dir_1/tF_5.txt:5
inner_dir_1/tF_5.txt:6
inner_dir_1/tF_5.txt:7
inner_dir_1/tF_5.txt:8
inner_dir_1/tF_5.txt:9
inner_dir_1/tF_5.txt:10
inner_dir_1/tF_5.txt:11
inner_dir_1/tF_5.txt:12
inner_dir_1/tF_5.txt:13
tf_2.txt:the sec 3 
tf_2.txt:the SeCoNd 2
```
## 32. Find only the names and paths of files that do not contain the combination "second":
```
~/lentochka_7/homework_2/dir_1 
grep -rvL "second" ./*  
                                                                          
./inner_dir_1/tf_4.txt
./tf_1.txt
```
## 33. Display the last 4 lines of any text file in the terminal:
```
~/lentochka_7/homework_2/dir_1 
tail -n4 inner_dir_1/tf_3.txt  
                                                                     
Software testing principles
the second 2
the sec 2
the SeCoNd 2
```
## 34. Display the first 4 lines of any text file in the terminal:
```
lentochka_7/homework_2/dir_1 
head -4 inner_dir_1/tf_3.txt    
                                                                     
WHAT TESTING IS AND WHERE IT CAME FROM
WHO IS A TESTER AND WHAT IS THEIR WORK
WHAT YOU NEED TO KNOW AND BE ABLE TO LEARN
MYTHS AND MISCONCEPTIONS ABOUT TESTING
```
## 35. One-line command. Create a folder and create a text file with content:
```
~/lentochka_7/homework_2/dir_1 
mkdir test && cat>test.txt                                                                         
hghgh
hghhg
hghgh
^C
```
## 36. One-line command. Move all text files that contain the word "sec" in their content to any single folder.
```
~/lentochka_7/homework_2/dir_1 
grep -rvl sec | xargs mv -t inner_dir_1    
                                                 
mv: 'inner_dir_1/tf_3.txt' and 'inner_dir_1/tf_3.txt' are the same file
mv: 'inner_dir_1/tF_5.txt' and 'inner_dir_1/tF_5.txt' are the same file
```
## 37. One-line command. Copy all text files that contain the word "sec" in their content to any single folder.
```
~/lentochka_7/homework_2/dir_1 
grep -rvl sec | xargs cp -t inner_dir_1    
                                                    
cp: 'inner_dir_1/tf_3.txt' and 'inner_dir_1/tf_3.txt' are the same file
cp: 'inner_dir_1/test.txt' and 'inner_dir_1/test.txt' are the same file
cp: 'inner_dir_1/tF_5.txt' and 'inner_dir_1/tF_5.txt' are the same file
cp: 'inner_dir_1/tf_2.txt' and 'inner_dir_1/tf_2.txt' are the same file
```
## 38. One-line command. Find all lines with "sec" in all text files, copy and paste these lines into one newly created text file.
```
grep -rwl sec >>cat.txt 
```
## 39. One-line command. Delete text files that contain the word "sec" in their content.
```
~/lentochka_7/homework_2/dir_1 
grep -rwl sec |xargs rm 
```
## 40. Simply output the string "Good job!!" to the terminal.
```
~/lentochka_7/homework_2/dir_1 
echo 'Good job!!'  
                                                                               
Good job!!
```
