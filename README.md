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

```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta

```
### Display the content of the files
cat < file1
## OUTPUT

![Screenshot from 2025-02-25 14-40-51](https://github.com/user-attachments/assets/df35694f-17bb-4d91-9c29-e4aa759a6146)


cat < file2
## OUTPUT

![Screenshot from 2025-02-25 14-43-26](https://github.com/user-attachments/assets/03d7f74a-0db9-474d-bf95-18d6aa17237b)


# Comparing Files
cmp file1 file2

## OUTPUT

![Screenshot from 2025-02-25 14-44-46](https://github.com/user-attachments/assets/9a8e4c6b-c21d-4b10-b754-c354ac826ee9)


 
comm file1 file2
 ## OUTPUT

![Screenshot from 2025-03-04 14-06-40](https://github.com/user-attachments/assets/05560e0e-7742-4e60-a296-67e3b5cce37f)


 
diff file1 file2
## OUTPUT

![Screenshot from 2025-02-25 14-46-39](https://github.com/user-attachments/assets/bcd1026d-0fd4-4ba9-b7af-0e4263dac63c)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world

```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer

```


cut -c1-3 file11
## OUTPUT

![Screenshot from 2025-03-04 14-10-05](https://github.com/user-attachments/assets/be4bb260-864d-4610-960f-7168fba40829)


cut -d "|" -f 1 file22
## OUTPUT


![Screenshot from 2025-03-04 14-12-05](https://github.com/user-attachments/assets/9612c480-b3ab-4575-94c0-049a331bfb4f)



cut -d "|" -f 2 file22
## OUTPUT


![Screenshot from 2025-03-04 14-12-50](https://github.com/user-attachments/assets/d149406b-8e8f-4b82-abc1-dac66dd57010)



cat > newfile 
```
Hello world
hello world

````
cat < newfile 
```
Hello world
hello world
 ```

grep Hello newfile 
## OUTPUT


![Screenshot from 2025-03-04 14-22-17](https://github.com/user-attachments/assets/a0bf9edf-73e0-47d5-85f8-33429a00ff18)



grep hello newfile 
## OUTPUT


![Screenshot from 2025-03-04 14-22-50](https://github.com/user-attachments/assets/39ecdc56-ea12-412d-81ae-ba6c628e063c)



grep -v hello newfile 
## OUTPUT


![Screenshot from 2025-03-04 14-23-57](https://github.com/user-attachments/assets/2879f634-66e5-4ca2-9b4f-fc8d6d0d6615)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-03-04 14-24-49](https://github.com/user-attachments/assets/1e67c2c5-ec19-4cd3-9d13-5dff49ddb31b)



cat newfile | grep -i -c "hello"
## OUTPUT


![Screenshot from 2025-03-04 14-25-29](https://github.com/user-attachments/assets/a4972d98-1286-4a1e-81b8-88612413633a)



grep -R ubuntu /etc
## OUTPUT


![Screenshot from 2025-03-04 14-29-33](https://github.com/user-attachments/assets/ff69d166-c553-4beb-9fb9-a14f16aae396)



grep -w -n world newfile   
## OUTPUT


![Screenshot from 2025-03-04 14-33-53](https://github.com/user-attachments/assets/a9ab71a7-bd63-4248-9acf-1ac793eaf9af)



cat > newfile 

```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World

```

cat < newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World

 ```
egrep -w 'Hello|hello' newfile 

## OUTPUT


![Screenshot from 2025-03-04 14-36-10](https://github.com/user-attachments/assets/786e47f6-5e85-4041-906a-d6740e931549)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-03-04 14-37-00](https://github.com/user-attachments/assets/58a33556-cc63-4b49-8c27-fe02b1664c1e)



egrep -w '(H|h)ell[a-z]' newfile 

## OUTPUT

![Screenshot from 2025-03-04 14-38-41](https://github.com/user-attachments/assets/96938e0c-bb3a-4b7c-8005-c8c94241e99e)



egrep '(^hello)' newfile 

## OUTPUT


![Screenshot from 2025-03-04 14-39-29](https://github.com/user-attachments/assets/55e2176c-eae9-4738-8b9c-5595136f4b86)



egrep '(world$)' newfile 

## OUTPUT

![Screenshot from 2025-03-04 14-40-39](https://github.com/user-attachments/assets/e001c4e8-e824-4201-809c-04805053432a)



egrep '(World$)' newfile 

## OUTPUT


![Screenshot from 2025-03-04 14-41-25](https://github.com/user-attachments/assets/542dc743-8a24-4c47-986f-dac3ac793ae4)


egrep '((W|w)orld$)' newfile 

## OUTPUT

![Screenshot from 2025-03-04 14-42-06](https://github.com/user-attachments/assets/ae984bfb-174b-45fc-b213-b9f021640841)



egrep '[1-9]' newfile 

## OUTPUT

![Screenshot from 2025-03-04 14-42-43](https://github.com/user-attachments/assets/4394e310-430e-4220-9551-f93fd2475e33)



egrep 'Linux.*world' newfile 

## OUTPUT

![Screenshot from 2025-03-04 14-43-23](https://github.com/user-attachments/assets/2210e2ad-c611-4eae-8f79-70a702852691)


egrep 'Linux.*World' newfile 

## OUTPUT


![Screenshot from 2025-03-04 14-43-57](https://github.com/user-attachments/assets/88fc6b7d-a5db-42d9-92c3-67f7641e5d5e)



egrep l{2} newfile

## OUTPUT

![Screenshot from 2025-03-04 14-44-56](https://github.com/user-attachments/assets/186f6cc2-bb22-45e9-9899-a7394967901b)


egrep 's{1,2}' newfile

## OUTPUT 


![Screenshot from 2025-03-04 14-46-47](https://github.com/user-attachments/assets/a9f9f9ea-725a-43a2-911f-37c466dd2ce3)


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

```


sed -n -e '3p' file23
## OUTPUT


![Screenshot from 2025-03-08 11-15-47](https://github.com/user-attachments/assets/ec4d25e0-91e8-4054-bc93-4041998166ea)



sed -n -e '$p' file23
## OUTPUT


![Screenshot from 2025-03-08 11-17-17](https://github.com/user-attachments/assets/5fc2e261-9b43-44e2-abc7-3bc468169173)


sed  -e 's/Ram/Sita/' file23
## OUTPUT


![Screenshot from 2025-03-08 11-18-30](https://github.com/user-attachments/assets/d3f1ee70-1c44-4f50-b38d-b9c8c61d82d8)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-08 11-19-13](https://github.com/user-attachments/assets/f2715c61-9248-41c5-8a1a-6a514326fc4c)


sed  '/tom/s/5000/6000/' file23
## OUTPUT


![Screenshot from 2025-03-08 11-19-51](https://github.com/user-attachments/assets/a5513e52-6dcf-488b-b351-03d9f288f261)



sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-03-08 11-20-34](https://github.com/user-attachments/assets/909deccb-c2a0-4ed4-9de3-317132a8b54d)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot from 2025-03-08 11-21-05](https://github.com/user-attachments/assets/2678862d-f7a0-47d1-82ad-3bbe52aa97c1)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-03-08 11-22-08](https://github.com/user-attachments/assets/93207dd2-2c0e-4874-8e59-e6488fa41dfc)


seq 10 
## OUTPUT

![Screenshot from 2025-03-08 11-22-54](https://github.com/user-attachments/assets/674c87f5-6851-4e94-9ea1-53c77ee30506)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-03-08 11-23-32](https://github.com/user-attachments/assets/ff235d28-571f-4ddc-8231-c97c4a3e6e19)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-03-08 11-24-11](https://github.com/user-attachments/assets/d0dc4d0b-75df-4172-b377-b31b45aea5e6)


seq 3 | sed '2a hello'
## OUTPUT


![Screenshot from 2025-03-08 11-24-43](https://github.com/user-attachments/assets/15ef60bf-f4dc-4186-ac85-f35e644cfca2)



seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2025-03-08 11-25-19](https://github.com/user-attachments/assets/fbdc6bd7-9f7e-4e0a-a20d-e2ecdac057b0)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2025-03-08 11-25-49](https://github.com/user-attachments/assets/bf3c1d2a-debe-4984-a74d-6e8fe68ebfcb)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-03-08 11-26-25](https://github.com/user-attachments/assets/008850c5-b722-4050-b09c-36f10fecfb0c)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![Screenshot from 2025-03-08 11-28-10](https://github.com/user-attachments/assets/816dc2c8-4f98-44e4-8814-5d4bbe388c25)


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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
