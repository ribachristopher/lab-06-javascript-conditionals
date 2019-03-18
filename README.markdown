Lab - Permissions, Editing Text, Date and Time
==========
Follow the instructions line-by-line.  

* Type in the commands as is, but ignore the beginning prompt.  
* Enter, tab, up and down are represented by <ENTER><TAB>,<UP> and <DOWN>.  
* "No output" or "nothing happens" are valid answers to any of the questions.
* Whenever I ask "What is the command?", include any flags and arguments as well.
==========


==========
First, let's figure out what day and time it is!
==========

==========
1. What day and time is it?

What command did you use, and what was its output?
----------
date
Mon Mar 18 15:39:15 EDT 2019

==========
2. Print out a calendar for this month.

What command did you use, and what was its output?
----------
cal 
 March 2019       
Su Mo Tu We Th Fr Sa  
                1  2  
 3  4  5  6  7  8  9  
10 11 12 13 14 15 16  
17 18 19 20 21 22 23  
24 25 26 27 28 29 30  
31     


==========
3. a) Go to your home directory.  b) Verify that you're in your home directory.

What commands did you use to do this?
----------
cd ~


==========
4. a) Create an empty file called copy_to_backup.sh.  b) Verify that the file exists
What commands did you use to do this?
----------
touch copy_to_backup.sh.
ls
AMALogger20190109.log	AMALogger20190316.log	Public
AMALogger20190130.log	Adlm			QLData
AMALogger20190131.log	Adobe			Things
AMALogger20190201.log	Applications		__MACOSX
AMALogger20190204.log	Creative Cloud Files	copy_to_backup.sh.


==========
5. What are the permissions on copy_to_backup.sh.

What command did you use to find the permissions?
----------
ls -l
-rw-r--r--   1 student  staff        0 Mar 18 15:50 copy_to_backup.sh.


==========
6. a) Change the permissions so that copy_to_backup.sh is executable by the user.  b) Verify the new permissions.

What commands did you use to do this?  What was the output?
----------
chmod u+x copy_to_backup.sh.
-rwxr--r--   1 student  staff        0 Mar 18 15:50 copy_to_backup.sh.


==========
7. Try executing (running) the file!

$ ./copy_to_backup.sh

What command did you use to try to execute the file?  What happens?
----------
./copy_to_backup.sh
nothing happens


==========
8. Open copy_to_backup.sh with nano

What command did you use to do this?
----------
nano ./copy_to_backup.sh


==========
9. In copy_to_backup.sh, the very first line of your shell script should be:
#!/bin/bash

Then type, each on its on line, the commands to do the following:

a. Create a directory called backup in the CURRENT directory
b. Copy all of the txt files (use *.txt) in the current
   directory to the new backup directory
c. Print out "I'm done backing up"

The current directory means wherever you happen to be running the commands.

Write out the code in your file below...
----------
mkdir backup
cp *.txt
echo "I'm done backing up"


==========
10. Create a directory in your HOME called test
----------



==========
11. Go into the test directory and create two empty files... 1.txt and 2.txt

What commands did you use to do this?
----------
student$ touch 1.txt
ent-v314-016:test student$ touch 2.txt


==========
12. Move the script that you created into this directory.

What commands did you use to do this?
----------
mv copy_to_backup.sh test/


==========
13. Run your script.

What commands did you use to do this?
----------
./copy_to_backup.sh


==========
14. Verify that a backup folder was created in your test directory... with copies of the files present.

What commands did you use to do this?  Show the output.
----------
./copy_to_backup.sh 
Create directory backup
mkdir: backup: File exists
Copying all text files
I'm done backing up
ent-v314-016:test student$ ls
1.txt			backup
2.txt			copy_to_backup.sh

cd backup
ls
1.txt	2.txt

pwd
/Users/student/test/backup
