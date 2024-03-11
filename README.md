
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
![Screenshot from 2024-02-25 15-23-53](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/4c34dd00-397e-4acd-a459-c859faf65ed2)



cat < file2
## OUTPUT
![Screenshot from 2024-02-25 15-26-13](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/f64a137d-62da-4bce-ad90-c9dabf82f8e3)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![output os 1](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/e28ef4d4-0ed7-431c-b00f-3fe0f44ac8e7)

comm file1 file2
 ## OUTPUT
![output os 2](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/4f457834-fb32-4be8-8045-f62f3dfdfe09)

 
diff file1 file2
## OUTPUT
![output os 3](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/54df877d-037e-4d37-99e3-e9fed6774260)


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
![output os 4](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/4de8c82f-1b76-4d32-9a4a-fa0808132dc1)




cut -d "|" -f 1 file22
## OUTPUT
![output os 5](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/9928dbe7-eda1-481d-b4f4-52e60dd7e78a)



cut -d "|" -f 2 file22
## OUTPUT
![output os 6](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/7bb724a3-1345-42a0-851d-8a334a1cfafd)


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
![output os 7](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/f22f89b9-c3f2-47b7-834f-e184d8fe38da)



grep hello newfile 
## OUTPUT
![output os 8](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/fbfc5413-1afd-4083-b537-36692b8ad821)




grep -v hello newfile 
## OUTPUT
![output os 9](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/56eb9001-cc39-4450-964a-5f53f01e6ec0)



cat newfile | grep -i "hello"
## OUTPUT
![output os 10](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/e4a62690-4115-46b1-b604-5098932fee0a)




cat newfile | grep -i -c "hello"
## OUTPUT
![output os 11](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/d00a103e-4fef-4fad-8c84-2d3a59fa3f6c)




grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2024-02-25 15-31-57](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/b21b7da6-729a-45f1-bec4-ff6b9effd99c)



grep -w -n world newfile   
## OUTPUT
![output os 13](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/aaa267df-6e1f-412b-9f9c-82152a321146)


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
![output os 14](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/0a761b88-ccc0-457a-8d2c-d932fdb2ce0c)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![output os 15](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/a6a9648e-edbb-4d2a-b691-0868fafb5e2e)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![output os 16](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/c1b07d0e-fb7a-460e-b483-a5406064b2fe)




egrep '(^hello)' newfile 
## OUTPUT
![output os 17](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/ed8ed8cf-803f-4bbe-9e8c-4e442c2e17af)



egrep '(world$)' newfile 
## OUTPUT
![output os 18](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/6cfebe7e-506a-478c-acc4-e043af4c541c)



egrep '(World$)' newfile 
## OUTPUT
![output os 19](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/be80c0a9-328d-467c-bc98-89788310743d)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![output os 20](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/3793dc23-d103-40d5-9063-a9381869cb49)



egrep '[1-9]' newfile 
## OUTPUT
![output os 21](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/00a86c6c-ba76-4165-ad11-59d3d4d4af10)



egrep 'Linux.*world' newfile 
## OUTPUT
![output os 22](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/1f1213e7-2332-4b09-8e19-848e11e181f0)


egrep 'Linux.*World' newfile 
## OUTPUT
![output os 23](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/ab478792-c42f-4445-b1a2-440ff695da03)


egrep l{2} newfile
## OUTPUT
![output os 24](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/5a44dd5b-69cc-48a5-aea1-0845340a9c61)



egrep 's{1,2}' newfile
## OUTPUT 
![output os 25](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/0885bcb9-919a-4121-8b62-74b8c009f624)


cat > file22
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


sed -n -e '3p' file22
## OUTPUT
![output os 26](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/a513754b-cf31-4ed1-acf3-ef00c43489dc)



sed -n -e '$p' file22
## OUTPUT
![output os 27](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/2f52bda9-c176-4d5c-8e9b-16e1f6fd9ef7)



sed  -e 's/Ram/Sita/' file22
## OUTPUT
![output os 28](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/79c77842-269c-463f-941e-7c0309436900)



sed  -e '2s/Ram/Sita/' file22
## OUTPUT
![output os 29](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/2466363f-9b1c-43e3-b99e-4ec92e5308b8)



sed  '/tom/s/5000/6000/' file22
## OUTPUT
![output os 30](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/405cd5a4-e05f-4727-83ea-f6342462cee9)



sed -n -e '1,5p' file22
## OUTPUT
![output os 31](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/13796c7c-1769-4f0f-b67f-ec712ea606bd)



sed -n -e '2,/Joe/p' file22
## OUTPUT
![output os 32](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/21d301d2-34a9-4fee-9b1c-f5b2f7ee0c89)




sed -n -e '/tom/,/Joe/p' file22
## OUTPUT
![output os 33](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/a2a87c87-9e0b-4e95-af6c-ea31f54f16a5)



seq 10 
## OUTPUT
![output os 34](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/bcc3d504-bb73-4dea-96a7-b3f8426171b7)



seq 10 | sed -n '4,6p'
## OUTPUT
![output os 35](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/a5aa4533-52ef-41ef-88dc-5163706d6ba3)



seq 10 | sed -n '2,~4p'
## OUTPUT
![output os 36](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/67dc5a22-14aa-4adc-8517-bd7cfb63c68e)



seq 3 | sed '2a hello'
## OUTPUT
![output os 37](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/016e5dcf-ac27-45fc-86e1-6afa139c4cf6)



seq 2 | sed '2i hello'
## OUTPUT
![output os 38](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/54518b9c-4627-43ff-83b3-0e18403d5285)


seq 10 | sed '2,9c hello'
## OUTPUT
![output os 39](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/33c73d05-ef2c-48e1-a8c5-be4979946e86)


sed -n '2,4{s/^/$/;p}' file22
## OUTPUT
![output os 40](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/d5ed9af0-a6fa-4950-af0e-c7326f0d23e4)



sed -n '2,4{s/$/*/;p}' file22
## OUTPUT
![output os 41](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/83b645f4-f870-4352-ba30-9556bede4746)


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
![output os 42](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/8d80c952-66f4-41da-a538-bfaa6d2e568d)


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
![output os 43](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/949d21fe-620b-4f94-aac3-528743bd4a2e)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![output os 44](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/bbacc088-5799-46db-a898-b71da63a5d28)

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
![output os 45](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/c0f73c0b-1055-4c31-8bdd-2a368649eabc)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![output os 46](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/1655fa9a-c163-4677-8fd2-b58545573d3c)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
```
bench.py
file1
file11
file2
file21
file22
file23
hello.c
hello.js
newfile
readme.txt
urllist.txt
```

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
```
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt
drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/
-rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt
-rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt
```

tar -xvf backup.tar
## OUTPUT
```
x file1.txt
x directory1/
x directory1/file2.txt
x directory1/file3.txt
```

gzip backup.tar

ls .gz
## OUTPUT
```
 backup.tar.gz
```
 
gunzip backup.tar.gz
## OUTPUT
```
backup.tar
```

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2024-02-26 19-49-01](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/cd6aa88e-aa03-4879-8eac-096a80a8bf1a)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2024-02-26 19-51-06](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/7449297d-09c9-4e47-9593-2a2ae75545ea)


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
```
File name is ./scriptest.sh
File name is scriptest.sh
First arg. is 1
Second arg. is 2
Third arg. is 3
Fourth arg. is
The $@ is 1 2 3
The $\# is $#
The $$ is 124
```

 
ls file1
## OUTPUT
![Screenshot from 2024-02-26 19-53-14](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/c2ffd586-64f4-4d86-814f-53fd3b966af5)

echo $?
## OUTPUT 
![Screenshot from 2024-02-26 19-53-36](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/e004d6ed-48ab-45a6-bfd8-ab8faa8788b5)

 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
1

 
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
## OUTPUT
![Screenshot from 2024-02-26 20-02-51](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/669c08af-be10-452a-a16b-2d960c674987)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
```
baseball is less than hockey
```



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
```
You are the owner of the /etc/passwd file
```

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
![Screenshot from 2024-02-26 20-13-04](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/efa998fe-2806-4eca-ace7-1d71dda33cf6)



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
## OUTPUT
![Screenshot from 2024-02-26 20-15-44-1](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/545398c0-2c77-4e44-b53a-6ef098142c6f)


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
## OUTPUT
![Screenshot from 2024-02-26 20-18-03](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/3f9abd70-a9ff-43f5-9b46-39fd1f374d55)

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
```
Welcome Ram
Please enjoy your visit
Welcome Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here
```

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
![Screenshot from 2024-02-26 20-20-50](https://github.com/guru14789/OS-Linux-commands-Shell-script/assets/151705853/73bf26c3-76c2-4dbe-8aa4-213a1cef52fb)

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
## OUTPUT
```
Welcome Ram/Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here
```
 
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
 ## OUTPUT
 ```
 10
9
8
7
6
5
4
3
2
1
```
 
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
$ chmod 755 untiltest.sh
$ ./ untiltest.sh
 ## OUTPUT
 ```
 100
 75
 50
 25
```
 
 
 
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
$ ./forin1.sh
## OUTPUT
```
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado
```
 
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
## OUTPUT
```
word:I
word:dont know if thisll
word:work
```
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ ./forin3.sh
## OUTPUT
```
word:I
word:don't
word:know
word:if
word:this'll
word:work
```


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
```
Visit beautiful Hyderabad
Visit beautiful Alampur
Visit beautiful Basara
Visit beautiful Warangal
Visit beautiful Adilabad
Visit beautiful Bhadrachalam
Visit beautiful Khammam
```

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
```
The value of i is 1
The value of i is 2
The value of i is 3
The value of i is 4
The value of i is 5
```

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
```
1 - 5
2 - 4
3 - 3
4 - 2
5 - 1
```
 
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
$ chmod 755 forbreak.sh
$ ./forbreak.sh 
## OUTPUT
```
Iteration number: 1
Iteration number: 2
The for loop is completed
```
 
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
```
Iteration number: 1
Iteration number: 2
Iteration number: 4
Iteration number: 5
The for loop is completed
```
 
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
```
Enter your name: John
Hello John, welcome to my program.
```


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
```
Enter your name: sanju
Hello sanju, welcome to my program.
```



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

 ./funcex.sh  
 ./funcex.sh 1 2
 ## OUTPUT
 ```
$ bash script.sh 1 2
The result is 2
```

 
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
```
1
2
3
```
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
```
1
2
3
```
 
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
```
+ (( 0 ))
+ set +x
```
 
 
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
```
total characters 75
Number of Lines are 10
No of Words count: 10
```
 
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
```
Enter the number
121
Number is palindrome
Enter the number
69
Number is NOT palindrome
```


# RESULT:
The Commands are executed successfully.
