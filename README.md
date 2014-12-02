Project_CATE
============
##Preface
Hello to all you hackers out there, we are Jason and Amey, computer science students at Imperial College London. The main motivation behind this project was to write an interface which made accessing CATE (an online management system for DOC) and using its functionality easier.

This program has been written in C++.

##What is the latest version?
CATE BETA

##How to install?
For beta version, you will have to download the source code and compile it yourself in order to use it.

Type in the following to the terminal:
```bash
> cd {{your desired directory}}
> git clone https://github.com/ImperialUndergroundHacker/Project_CATE.git
> g++ Project_CATE/cate.cpp -o cate
```

After performing the above commands, your cate is ready on your machine! You can call it using:
```bash
> ./cate
```

##How to call the program with only "cate"?
There are two ways that we recommend to make the "cate" command recognisable by your machine.
###Build alias (work for labs machine)
To build an alias, perform the following command on the terminal:
Linux:
```bash
--Pre: the compiled cate file is at your current directory
> pwd | xargs -i echo "alias cate {}/cate" >> ~/.cshrc
> source ~/.cshrc
```
Mac:
```bash
--Pre: the compiled cate file is at your current directory
> pwd | xargs -i echo "alias cate={}/cate" >> ~/.bash_profile
> source ~/.bash_profile
```
###Copy it to "/bin" (require sudo)
To copy the file to the "/bin", perform the following command on the terminal:
```bash
--Pre: the compiled cate file is at your current directory
> sudo cp cate /bin
```
This command will require your password.

Your cate command is ready to go!
##How to use CATE?
All possible cate commands:

###cate update
Updates your computer with the latest changes on cate, for example if a new assignment has been uploaded.

###cate set <class> <period>
Sets your current class and period.
-eg. for Computing first year in autumn,type into terminal: cate set c1 1 for JMC first year in autumn, type into terminal:
```bashe
cate set j1 1
```

###cate ass
Lists the assignments for which the deadline has not passed, with their IDs and due date.

###cate ass -a
Lists all the assignments which are available on cate along with their IDs.

###cate mods
Lists all the modules for the current term, along with their module numbers.

###cate mods <modnumber>
Lists all the notes available for a specific module, along with the IDs.
-eg. type into terminal: cate mods 3

cate pull [<id>] Downloads files to your current directory, and
asks you if you want to print them. Input the
IDs of the files you wish to download.
eg. To download files s502, s545 and n19,
type into terminal: cate pull s502 s545 n19
where s502, s545 and n19 are IDs.

cate submit <id> Submits a programming assignment to cate. Right
after you push your work, just run this command
from your assignment's folder, and it will
handle the declaration submission and cate token
upload.

cate getcover [<id>] Handles the submission of non-programming
assignments. This will download the cover pages
and ask you if you want to print them.
eg. type into terminal: cate getcover s502 s545
