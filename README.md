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

<img width="692" height="297" alt="Screenshot 1" src="https://github.com/user-attachments/assets/1569309b-2db5-4fff-8e8b-0b22bbee568d" />


cat < file2
## OUTPUT

<img width="657" height="337" alt="Screenshot 2" src="https://github.com/user-attachments/assets/de2ee288-a54d-4147-91d8-367c9332bd2d" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="662" height="135" alt="Screenshot 3" src="https://github.com/user-attachments/assets/7cd9695a-3d07-487b-b200-54d4fae31d5f" />

comm file1 file2
 ## OUTPUT
<img width="717" height="577" alt="Screenshot 4" src="https://github.com/user-attachments/assets/dd1be51e-b33a-4765-a841-263a1dba920b" />

 
diff file1 file2
## OUTPUT
<img width="647" height="452" alt="Screenshot 5" src="https://github.com/user-attachments/assets/32cbc824-f76d-4715-a00a-532a45bf1eb6" />


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

<img width="695" height="175" alt="Screenshot 6" src="https://github.com/user-attachments/assets/114eb24b-86c1-4374-b1a1-1bcb1a0c2399" />



cut -d "|" -f 1 file22
## OUTPUT


<img width="595" height="222" alt="Screenshot 7" src="https://github.com/user-attachments/assets/33adba22-bb95-4481-be20-e3aa8c3e9b53" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="647" height="242" alt="Screenshot 8" src="https://github.com/user-attachments/assets/1a6f7be1-9407-479f-8926-4ce08b536f3f" />

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



grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT




cat newfile | grep -i -c "hello"
## OUTPUT




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT


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

<img width="361" height="91" alt="Screenshot 9" src="https://github.com/user-attachments/assets/29590de4-54e9-4865-8a0e-db7681a79c8a" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="361" height="91" alt="Screenshot 9" src="https://github.com/user-attachments/assets/5d49466e-3af3-4878-b763-630fe96fb06c" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT



<img width="395" height="92" alt="Screenshot 10" src="https://github.com/user-attachments/assets/04a278ff-8018-473f-88a4-dde041c2095f" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="336" height="77" alt="Screenshot 11" src="https://github.com/user-attachments/assets/e4cd0d9b-41ee-491f-abcf-da904f5bba08" />



egrep '(world$)' newfile 
## OUTPUT


<img width="355" height="100" alt="Screenshot 12" src="https://github.com/user-attachments/assets/3135517d-eee8-4387-a918-f7a7f0fed593" />

egrep '(World$)' newfile 
## OUTPUT

<img width="367" height="77" alt="Screenshot 13" src="https://github.com/user-attachments/assets/2f70787a-19d3-4cab-bcae-d926512cddb2" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="377" height="126" alt="Screenshot 14" src="https://github.com/user-attachments/assets/cb0eb36c-224c-40d7-b690-7eae00c0b506" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="332" height="72" alt="Screenshot 15" src="https://github.com/user-attachments/assets/951746c9-6b9f-4a7b-8238-6241ed681e3e" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="352" height="76" alt="Screenshot 16" src="https://github.com/user-attachments/assets/a569a8c0-3e67-442a-a2ae-418ea7bfbe39" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="337" height="67" alt="Screenshot 17" src="https://github.com/user-attachments/assets/0538e19c-1ec2-4785-96e7-8004e9760b3d" />

egrep l{2} newfile
## OUTPUT
<img width="355" height="92" alt="Screenshot 19" src="https://github.com/user-attachments/assets/712c1f7a-f2c4-4c3d-ab5e-017bc953b1a1" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="377" height="122" alt="Screenshot 20" src="https://github.com/user-attachments/assets/0f7c2b54-8be7-4ab0-93d9-fde5f00f365d" />


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


<img width="376" height="75" alt="Screenshot 21" src="https://github.com/user-attachments/assets/a4abb19d-e4b8-4d43-b112-93cd07b28519" />

sed -n -e '$p' file23
## OUTPUT

<img width="376" height="75" alt="Screenshot 21" src="https://github.com/user-attachments/assets/4497f789-2ab9-44d9-b1fa-9c00acc70891" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="375" height="250" alt="Screenshot 22" src="https://github.com/user-attachments/assets/55682c87-f9e9-4a57-985f-809f920b1ae8" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="402" height="252" alt="Screenshot 23" src="https://github.com/user-attachments/assets/0234053b-6771-4644-9024-c3ba31327752" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="411" height="246" alt="Screenshot 24" src="https://github.com/user-attachments/assets/db7cc1e1-5d43-49fd-85c4-5ed416bc5d2b" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="405" height="172" alt="Screenshot 25" src="https://github.com/user-attachments/assets/89798d0e-40a5-40f7-9637-1e6be873fd19" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="440" height="121" alt="Screenshot 26" src="https://github.com/user-attachments/assets/7df13e50-197a-4dfe-88f8-1cdf0eea23d3" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="450" height="107" alt="Screenshot 27" src="https://github.com/user-attachments/assets/b437470f-aa7a-4916-936e-65d73d082d4b" />


seq 10 
## OUTPUT

<img width="360" height="295" alt="Screenshot 28" src="https://github.com/user-attachments/assets/0120d109-16b5-4a10-909f-becb6d80c464" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="387" height="130" alt="Screenshot 29" src="https://github.com/user-attachments/assets/576b4a4f-b7fb-4dcf-a415-6d4ea2d609bf" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="406" height="122" alt="Screenshot 30" src="https://github.com/user-attachments/assets/81fa86d1-6109-44f5-aeb8-ba19a2854323" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="382" height="132" alt="Screenshot 31" src="https://github.com/user-attachments/assets/62e7cd54-056b-4cd3-a844-7df566cf013f" />


seq 2 | sed '2i hello'
## OUTPUT


<img width="362" height="130" alt="Screenshot 32" src="https://github.com/user-attachments/assets/7db62fd7-25c6-4fcf-898d-9b3c25924ed5" />
seq 10 | sed '2,9c hello'
## OUTPUT
<img width="415" height="120" alt="Screenshot 33" src="https://github.com/user-attachments/assets/379ed7bb-e634-464a-952b-8362b5530a88" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="445" height="117" alt="Screenshot 34" src="https://github.com/user-attachments/assets/3fd0f114-78ab-4609-9af5-24b93d55776a" />


sed -n '2,4{s/$/*/;p}' file23

<img width="425" height="127" alt="Screenshot 35" src="https://github.com/user-attachments/assets/24d82738-65b5-4d80-9a0f-4b4b691f3654" />

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

<img width="502" height="117" alt="Screenshot 39" src="https://github.com/user-attachments/assets/0b2e3678-ea8b-40b5-afb9-0319e1072019" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="347" height="242" alt="Screenshot 40" src="https://github.com/user-attachments/assets/ce9f75b1-f3a1-4879-84e2-7cadbdefd3c5" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="705" height="447" alt="Screenshot 41" src="https://github.com/user-attachments/assets/7499c4da-1ed4-419a-a411-7d85bd395043" />


tar -xvf backup.tar
## OUTPUT
<img width="487" height="252" alt="Screenshot 42" src="https://github.com/user-attachments/assets/237350ad-3e21-4194-a88c-d5dc73943d08" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="562" height="312" alt="Screenshot 43" src="https://github.com/user-attachments/assets/4e923fb8-d2d8-448d-8030-d1734a9d9fba" />

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

<img width="450" height="152" alt="Screenshot 44" src="https://github.com/user-attachments/assets/36773b86-d22f-4a3a-b125-31ad290db3f0" />

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

 <img width="477" height="322" alt="Screenshot 45" src="https://github.com/user-attachments/assets/e1345f02-6323-414f-96cd-1c61c6953628" />
 <img width="621" height="392" alt="Screenshot 46" src="https://github.com/user-attachments/assets/f9a06d91-3733-48ec-b071-421eb3c45f32" />


ls file1
## OUTPUT
<img width="367" height="72" alt="Screenshot 47" src="https://github.com/user-attachments/assets/b425b524-d29a-4aa1-8ca3-6fc50f270802" />

echo $?
## OUTPUT 
<img width="447" height="77" alt="Screenshot 48" src="https://github.com/user-attachments/assets/901d0b38-2744-493a-a6a1-fe1c0dc272e7" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="502" height="152" alt="Screenshot 49" src="https://github.com/user-attachments/assets/1c5105eb-441e-4a97-9b1d-ac2ec12bcca8" />

abcd
 
echo $?
 ## OUTPUT

<img width="467" height="156" alt="Screenshot 50" src="https://github.com/user-attachments/assets/e291f5b3-ed32-4b21-8989-87d95461b5e6" />

 
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

<img width="621" height="422" alt="Screenshot 51" src="https://github.com/user-attachments/assets/b90524bf-2b7b-46cd-a1d2-7a7934c367f1" />


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
<img width="617" height="306" alt="Screenshot 52" src="https://github.com/user-attachments/assets/e55c4a7e-7fb6-4719-983b-50b080ac37c5" />

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

<img width="601" height="547" alt="Screenshot 53" src="https://github.com/user-attachments/assets/9b9b2821-1868-4f4c-848d-def29c139690" />


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
<img width="605" height="532" alt="Screenshot 54" src="https://github.com/user-attachments/assets/cfd57c30-3f7f-4000-b5e8-08e842a2c54b" />

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
<img width="672" height="675" alt="Screenshot 55" src="https://github.com/user-attachments/assets/331a32ea-0fc8-4fcf-905c-d74a993c6901" />


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
<img width="677" height="680" alt="Screenshot 56" src="https://github.com/user-attachments/assets/8148b77c-c141-4428-aa1e-b9f3743e9140" />


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
<img width="676" height="377" alt="Screenshot 57" src="https://github.com/user-attachments/assets/8cbb197a-03d3-4e95-a377-84d204c061ab" />


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
 <img width="682" height="456" alt="Screenshot 58" src="https://github.com/user-attachments/assets/912f318b-8957-4be8-a5d4-e39135a8ca1c" />

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
 
 <img width="665" height="476" alt="Screenshot 59" src="https://github.com/user-attachments/assets/d96600ad-bb72-4810-a4e3-151adbd0c8bc" />

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
<img width="671" height="257" alt="Screenshot 60" src="https://github.com/user-attachments/assets/e7ba0b7b-e6dd-4b04-9a61-aeac549db2c1" />

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
