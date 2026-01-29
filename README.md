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
<img width="290" height="160" alt="Screenshot from 2026-01-29 18-30-27" src="https://github.com/user-attachments/assets/41501c51-25b4-4beb-9e8f-3489002242c5" />



cat < file2
## OUTPUT
<img width="322" height="177" alt="Screenshot from 2026-01-29 18-35-17" src="https://github.com/user-attachments/assets/ebde70c7-9ee2-45bc-b7c1-b3617d69683c" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="369" height="109" alt="Screenshot from 2026-01-29 18-36-40" src="https://github.com/user-attachments/assets/95556a0e-6cdb-4ad0-86d5-ce0129148715" />

 
comm file1 file2
 ## OUTPUT
 <img width="396" height="180" alt="Screenshot from 2026-01-29 18-38-25" src="https://github.com/user-attachments/assets/51603e6f-0e93-4d1a-88b5-02abed4d3222" />


 
diff file1 file2
## OUTPUT
<img width="394" height="225" alt="Screenshot from 2026-01-29 18-39-13" src="https://github.com/user-attachments/assets/47620eb3-4b6a-42b2-adda-c3b5ba56c44d" />



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
<img width="448" height="184" alt="Screenshot from 2026-01-29 18-42-43" src="https://github.com/user-attachments/assets/90ffa240-3ec4-4b5b-b298-92124f56aeb0" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="452" height="183" alt="Screenshot from 2026-01-29 18-46-30" src="https://github.com/user-attachments/assets/583ecc37-a679-48c9-af3d-d7c08aebd33f" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="423" height="97" alt="Screenshot from 2026-01-29 18-47-33" src="https://github.com/user-attachments/assets/93cd892e-040c-477d-8813-76a6c7f1040d" />



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
<img width="335" height="46" alt="Screenshot from 2026-01-29 18-51-40" src="https://github.com/user-attachments/assets/d1ddf388-1ef6-4298-86f7-e2e35b953e17" />





grep hello newfile 
## OUTPUT

<img width="335" height="46" alt="Screenshot from 2026-01-29 18-52-22" src="https://github.com/user-attachments/assets/39887a03-ebbc-4914-8649-c02ff4735f2f" />





grep -v hello newfile 
## OUTPUT
<img width="371" height="52" alt="Screenshot from 2026-01-29 18-54-07" src="https://github.com/user-attachments/assets/bad30608-c066-41e1-bd9a-e2880a0acab4" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="456" height="80" alt="Screenshot from 2026-01-29 18-55-25" src="https://github.com/user-attachments/assets/2e98c8c7-20d0-4935-adc5-717cd909bcb8" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="465" height="52" alt="Screenshot from 2026-01-29 18-58-16" src="https://github.com/user-attachments/assets/ac714a3e-3739-4d98-bc56-bb3b4e6816ae" />





grep -R ubuntu /etc
## OUTPUT
<img width="464" height="172" alt="Screenshot from 2026-01-29 19-04-32" src="https://github.com/user-attachments/assets/da84f34c-ce9f-4344-b76c-45162faa185a" />




grep -w -n world newfile   
## OUTPUT
<img width="469" height="73" alt="Screenshot from 2026-01-29 19-05-39" src="https://github.com/user-attachments/assets/ab65e211-9d5c-4633-92d2-bd39f85c95fd" />


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
<img width="469" height="73" alt="Screenshot from 2026-01-29 19-11-20" src="https://github.com/user-attachments/assets/7acff208-8084-4ef7-8fed-67a2ae6ff7c9" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="469" height="73" alt="Screenshot from 2026-01-29 19-19-10" src="https://github.com/user-attachments/assets/6c483c43-3b8d-46a2-92cd-63a2a51b26ea" />





egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="469" height="73" alt="Screenshot from 2026-01-29 19-13-29" src="https://github.com/user-attachments/assets/b3b448f6-6118-4de5-b6b9-c083367a3876" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="478" height="50" alt="Screenshot from 2026-01-29 19-20-27" src="https://github.com/user-attachments/assets/ebccae4c-34c6-4f61-9890-2658d9782dba" />




egrep '(world$)' newfile 
## OUTPUT
<img width="416" height="140" alt="Screenshot from 2026-01-29 19-24-19" src="https://github.com/user-attachments/assets/a0f95622-624a-4ead-ac2c-20e4c1db23d7" />




egrep '(World$)' newfile 
## OUTPUT
<img width="416" height="140" alt="Screenshot from 2026-01-29 19-24-19" src="https://github.com/user-attachments/assets/7cde73b6-4a88-420a-891e-11f282f3763e" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="485" height="74" alt="Screenshot from 2026-01-29 19-27-55" src="https://github.com/user-attachments/assets/3a9ff82e-c399-48c4-88f7-63247b4118ed" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="506" height="56" alt="Screenshot from 2026-01-29 19-28-47" src="https://github.com/user-attachments/assets/1c50b945-050e-4c1b-b391-64a0e1a6dd23" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="506" height="56" alt="Screenshot from 2026-01-29 19-56-58" src="https://github.com/user-attachments/assets/815cc230-a587-4f79-b072-5ea46386e1eb" />




egrep 'Linux.*World' newfile 
## OUTPUT
<img width="506" height="56" alt="Screenshot from 2026-01-29 19-56-58" src="https://github.com/user-attachments/assets/0eddea12-78ae-469d-a667-d7db821af4af" />


egrep l{2} newfile
## OUTPUT
<img width="507" height="73" alt="Screenshot from 2026-01-29 19-59-02" src="https://github.com/user-attachments/assets/73ddd9e4-3eea-4d28-986a-b15e382dc579" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="512" height="93" alt="image" src="https://github.com/user-attachments/assets/7a5e60c7-6d2a-447b-9a71-faf0e56e65dd" />


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
<img width="512" height="60" alt="Screenshot from 2026-01-29 20-22-40" src="https://github.com/user-attachments/assets/8d7af35b-49be-4344-8947-ecc1510e67e1" />




sed -n -e '$p' file23
## OUTPUT
<img width="512" height="48" alt="Screenshot from 2026-01-29 20-24-11" src="https://github.com/user-attachments/assets/9b9bec6f-32ba-4cea-bc67-7b9f18433726" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="504" height="214" alt="Screenshot from 2026-01-29 20-26-38" src="https://github.com/user-attachments/assets/f773a4cc-44e6-4607-8766-a449f1eea746" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="486" height="212" alt="Screenshot from 2026-01-29 20-28-19" src="https://github.com/user-attachments/assets/630ef8bf-c3b5-4384-bc0b-975ad2366f73" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="486" height="206" alt="Screenshot from 2026-01-29 20-29-47" src="https://github.com/user-attachments/assets/14850a6d-7f24-4859-a181-f540323540a4" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="483" height="143" alt="Screenshot from 2026-01-29 20-30-50" src="https://github.com/user-attachments/assets/61b9d36a-aaa6-4c28-b417-32390250fa41" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="483" height="105" alt="Screenshot from 2026-01-29 20-31-42" src="https://github.com/user-attachments/assets/e9159c8c-2077-4d95-b798-cf9964f581b1" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="490" height="78" alt="Screenshot from 2026-01-29 20-32-45" src="https://github.com/user-attachments/assets/3e2983e3-693f-4588-a6fb-1546ca601c55" />



seq 10 
## OUTPUT
<img width="490" height="254" alt="Screenshot from 2026-01-29 20-33-15" src="https://github.com/user-attachments/assets/880d8d71-1ae7-43eb-9397-987db166b674" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="490" height="104" alt="Screenshot from 2026-01-29 20-35-13" src="https://github.com/user-attachments/assets/098c8ea8-332b-43dd-8d27-4249112dda23" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="490" height="104" alt="Screenshot from 2026-01-29 20-36-15" src="https://github.com/user-attachments/assets/302d2fd9-1d85-46b9-ac2c-3372624e4960" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="490" height="130" alt="Screenshot from 2026-01-29 20-37-59" src="https://github.com/user-attachments/assets/94e378f5-13ca-4017-aafc-879bfe98cbfa" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="490" height="130" alt="Screenshot from 2026-01-29 20-38-47" src="https://github.com/user-attachments/assets/649aeda6-3f86-4827-8adc-7fa9dfb3a466" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="490" height="130" alt="Screenshot from 2026-01-29 20-40-14" src="https://github.com/user-attachments/assets/0ac7d525-49f2-4187-ae74-51c10af335f4" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="490" height="130" alt="Screenshot from 2026-01-29 20-42-29" src="https://github.com/user-attachments/assets/96ae021f-cf1e-4169-a826-ade3d08e12e4" />




sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="490" height="130" alt="Screenshot from 2026-01-29 20-45-07" src="https://github.com/user-attachments/assets/0829f237-792e-4873-aa3f-1ffc60ab6091" />




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
<img width="490" height="130" alt="Screenshot from 2026-01-29 20-52-35" src="https://github.com/user-attachments/assets/5a12a4ce-de85-4940-8d42-220a011eb053" />




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
<img width="490" height="130" alt="Screenshot from 2026-01-29 21-02-09" src="https://github.com/user-attachments/assets/bcb65f4f-5e12-4e3d-a088-b597574ca455" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="490" height="174" alt="Screenshot from 2026-01-29 21-05-14" src="https://github.com/user-attachments/assets/800d604a-6fd5-4ce3-ba7c-ffdc436f7d8f" />


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
<img width="406" height="129" alt="Screenshot from 2026-01-29 21-08-35" src="https://github.com/user-attachments/assets/dede7e8f-21c1-40e2-a7a9-bdf6984181e7" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="406" height="129" alt="Screenshot from 2026-01-29 21-10-30" src="https://github.com/user-attachments/assets/d0fb551e-6dba-43fd-98ff-e460a51e4b58" />




#Backup commands
tar -cvf backup.tar *



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="406" height="129" alt="Screenshot from 2026-01-29 21-43-26" src="https://github.com/user-attachments/assets/6e9fce6e-5ece-49d3-905d-18d7083042ff" />


tar -xvf backup.tar
## OUTPUT
<img width="403" height="143" alt="Screenshot from 2026-01-29 21-45-45" src="https://github.com/user-attachments/assets/a5075619-75ba-42e5-ab9d-3075ba2b3fc3" />


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
