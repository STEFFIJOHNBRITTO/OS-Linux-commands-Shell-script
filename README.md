# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![Screenshot from 2024-02-19 16-22-51](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/c35eee39-b77b-42f5-ae91-42caecdd52da)


cat < file2
## OUTPUT
![Screenshot from 2024-02-19 17-28-31](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/682bbd9a-6678-4624-b5f7-6daaf396807c)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2024-02-19 17-32-20](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/8640faa3-8194-4ee4-a16c-dd365e6905ec)

comm file1 file2
 ## OUTPUT
![Screenshot from 2024-02-19 17-35-16](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/71f6a18b-cb96-46ac-b04c-8a90319de369)

 
diff file1 file2
## OUTPUT
![Screenshot from 2024-02-19 21-06-13](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/59e72bbd-0260-45a8-b1a4-1b685695971c)



#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![Screenshot from 2024-02-19 21-09-44](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/2464b3f4-6b08-41be-aa67-e117fd96dfc1)




cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2024-02-19 21-10-52](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/86de4428-9ee0-485d-9696-cbac521429a0)


cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2024-02-19 21-23-06](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/68a6922d-20c0-4af8-921a-d7a14af1d483)

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-33-58](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/5225be44-5ded-479f-81c0-1b08a43a3db2)



grep hello newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-35-38](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/78ef312e-f2f6-4d3d-a656-eb5f93641a61)




grep -v hello newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-36-08](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/2e1628ca-d122-4a5c-8616-8c6c318f224b)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2024-02-19 21-36-39](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/79b59c5f-d111-43af-a1b8-1cd24831653c)



cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2024-02-19 21-37-05](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/fd5bc91e-6d16-42f4-913b-8baedfae7d67)




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2024-02-19 21-42-45](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/10e88fba-0b66-41aa-bf4d-1eec3ec8bb73)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-46-41](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/2f7618eb-26c9-4a06-b037-6e2a05e035a8)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-49-41](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/1586acca-2c82-4c42-98bc-4ae798eef1a8)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2024-02-19 21-52-25](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/8688c525-73fb-44c1-aedc-42c6bf61741e)



egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-52-49](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/4980783d-eee0-4468-a932-ed98b32fb05f)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-53-18](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/0c3b9da2-1ec3-4ed6-afdf-d97b3ec65697)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-53-48](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/69094a6a-7169-4233-8e34-b63fd3b50f86)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-54-11](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/228361e3-4c51-408b-acae-b547654c8d92)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-54-38](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/78841f5b-a1d6-42da-a170-f873f2db1c02)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-55-00](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/218b2ba3-76f4-4fe8-8822-3d64fc006de9)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2024-02-19 21-55-18](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/e0fb9fd4-0e34-4bb0-b447-480e7353e23c)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2024-02-19 21-55-54](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/455cefd1-c3cf-4a56-9626-22f5acc9d758)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-02-19 21-56-46](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/8b7b973d-2ecb-4adf-b3b0-b4a6090238f4)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![Screenshot from 2024-02-19 22-03-40](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/6ed8eeb2-98aa-489d-b7b5-502fad1fa948)



sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2024-02-19 22-04-04](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/a525b7f6-5451-4607-bf43-47e41df195cc)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2024-02-19 22-04-27](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/2dec5d41-9a09-4e5e-8b9e-124614c5ba56)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-02-19 22-04-47](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/18fb9a8e-d5ce-4f68-8d04-799b2e781cd6)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2024-02-19 22-05-04](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/5209fed2-c815-4dd9-bbfc-885f9104d28a)



sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2024-02-19 22-05-27](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/59481f62-1000-4099-be96-30a15f0f9f9f)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2024-02-19 22-06-07](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/c1935ffc-35e7-488e-a332-e3dd4c0b4220)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-02-19 22-09-55](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/3156abad-90b0-40bc-82f2-7e288e6776c9)



seq 10 
## OUTPUT

![Screenshot from 2024-02-19 22-10-26](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/ea0f93d4-b7fe-4b56-83f8-5df261f74fcb)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2024-02-19 22-13-29](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/bc5e24b5-5130-4756-b972-bd061802099e)


seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2024-02-19 22-13-48](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/af99d8d5-a0fb-4a3f-8391-4ce396c27f9f)



seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2024-02-19 22-14-24](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/ebff4972-2af6-4823-8af3-5a2218ed0f9e)


seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2024-02-19 22-14-48](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/6a7d5a34-213f-4d78-a264-72be126d9325)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2024-02-19 22-15-21](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/56f96442-9167-4513-812b-07e8b22b9252)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2024-02-19 22-15-43](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/cbadd6df-119c-4a6a-b7ac-8888a033311e)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT:
![Screenshot from 2024-02-19 22-16-01](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/36d38ad5-fd86-4e5d-86f3-734e1c0390bc)



#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![Screenshot from 2024-02-19 23-32-00](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/b947d6ba-4de8-436b-a7b7-fd88455c4fa3)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![Screenshot from 2024-02-19 23-33-39](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/df15d132-7d04-43d4-ae87-87bb88a3e002)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2024-02-19 23-35-40](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/2fe37e25-e5ba-4bbb-9209-9980e7b79ff5)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![Screenshot from 2024-02-19 23-38-44](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/3d90c98b-a7b3-43f6-8674-b310a5ab193b)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2024-02-19 23-40-24](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/ca555058-30ad-4a25-899a-81179c28d117)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2024-02-24 10-23-11](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/d813cb49-6684-4e3c-8570-ea7d6368b688)

![Screenshot from 2024-02-24 10-23-40](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/70216941-d36d-4b4a-88a5-8243e9fd3ebf)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


![Screenshot 2024-03-01 230259](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/37e150f1-0f45-459a-8e02-bc6930305f76)

![Screenshot 2024-03-01 230336](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/608c8fbd-a025-4e20-bde0-f22c15a970ba)


tar -xvf backup.tar
## OUTPUT

![Screenshot 2024-03-01 230559](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/6d15dda7-af04-4b2e-b963-f5f1a3afd6fa)

gzip backup.tar

ls .gz
## OUTPUT

 
gunzip backup.tar.gz
## OUTPUT
![Screenshot 2024-03-01 230623](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/02b19e22-66a3-44f7-82c2-d9260d8541b8)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![Screenshot 2024-03-01 231849](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/16a22c73-4ec8-45d9-ad96-f3837d97ef21)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2024-03-01 231904](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/01fd5fa5-bc1b-4b4f-b53d-a5eb47c370f2)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![Screenshot 2024-03-01 232223](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/3ae2e4aa-5de7-4cdf-a301-6264eaec0ed7)

 
ls file1
## OUTPUT
![Screenshot 2024-03-01 232248](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/38f79edd-2d9e-445b-93b1-015b9904ab49)

echo $?
## OUTPUT 
![Screenshot 2024-03-01 232303](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/10828a0c-d40f-4029-91e2-f13a6e9be2db)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![Screenshot 2024-03-01 232321](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/84e497a4-8320-47a0-9728-2e5251c7fed4)

abcd
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
![Screenshot 2024-03-01 232348](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/6fc306db-96b2-4f39-a304-4f03bab7f0ad)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot 2024-03-01 232421](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/d5d0cf5f-fb0c-40d6-a992-f97d69de5d2e)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![Screenshot 2024-03-01 232434](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/d6becc54-422c-4184-9555-ca5d543aaff5)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

![Screenshot 2024-03-01 232449](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/be26ce19-6dd8-4160-904a-55004860593c)


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
![Screenshot 2024-03-01 232502](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/bffb9936-3585-48c3-a587-911a8e628d37)

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![Screenshot 2024-03-01 232939](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/bd2057f0-f0fd-49fa-bd6e-f30e6d48c62b)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![Screenshot 2024-03-01 232953](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/7ebd4cf9-99c6-4081-a7bc-bfaed03a2e17)


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![Screenshot 2024-03-01 233023](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/584ef834-c04a-4afd-b92e-318deba3d677)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 ![Screenshot 2024-03-01 233107](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/81d3e9d1-aef2-4da1-889e-ace086eb57ee)

cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 # RESULT

 The output of the given program is executed successfully
