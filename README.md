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
![Screenshot 2025-05-21 152910](https://github.com/user-attachments/assets/0da9f6a3-c1a0-4246-ac91-b826379caa64)




cat < file2
## OUTPUT
![Screenshot 2025-05-21 153117](https://github.com/user-attachments/assets/a7720152-2af0-497f-b692-1e30ddbcb5e6)



# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2025-05-21 153243](https://github.com/user-attachments/assets/8101e3f5-e4ed-4c26-8f10-4a9c7f514ca7)

 
comm file1 file2
 ## OUTPUT
 ![Screenshot 2025-05-21 153444](https://github.com/user-attachments/assets/a54982bb-ba54-4385-85a9-4e425dd43a28)


 
diff file1 file2
## OUTPUT
![Screenshot 2025-05-21 153524](https://github.com/user-attachments/assets/311efb66-2b73-412e-8acc-16efc38263c7)



#Filters

### Create the following files file11, file22 as follows:

cat > file11
Hello world
This is my world
^d


cat > file22

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d



cut -c1-3 file11
## OUTPUT
![Screenshot 2025-05-21 153723](https://github.com/user-attachments/assets/c2af6cc5-4d20-4186-90e7-8dd3c5eeda2c)





cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2025-05-21 211056](https://github.com/user-attachments/assets/811fb123-c966-46f6-9b13-f253c7eff09c)




cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-05-21 211220](https://github.com/user-attachments/assets/97dde19e-6579-4267-ab68-8bea2ddfb645)



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
![Screenshot 2025-05-21 211319](https://github.com/user-attachments/assets/530cdf63-a0af-4e30-aa73-d3079c0d48c7)




grep hello newfile 
## OUTPUT
![Screenshot 2025-05-21 211420](https://github.com/user-attachments/assets/94f06d27-adee-4869-a594-1ec21918e57b)





grep -v hello newfile 
## OUTPUT
![Screenshot 2025-05-21 211629](https://github.com/user-attachments/assets/45e4afdf-5ade-4507-863d-c25950d5c241)




cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2025-05-21 211655](https://github.com/user-attachments/assets/a561f571-082d-41ff-8827-69f82bf7ac0b)





cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2025-05-21 212026](https://github.com/user-attachments/assets/34f8ff4f-cf93-46cb-8338-6174b7c0a842)





grep -R ubuntu /etc
## OUTPUT
![Screenshot 2025-05-21 212058](https://github.com/user-attachments/assets/11f22bf3-6871-43d4-a3cf-ef862c434736)





grep -w -n world newfile   
## OUTPUT
![Screenshot 2025-05-21 212159](https://github.com/user-attachments/assets/713a90ae-a88b-4278-9510-d01ab810845e)



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
![Screenshot 2025-05-21 212234](https://github.com/user-attachments/assets/4b5f1096-55f9-4f35-8343-5d90de2ad445)




egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot 2025-05-21 212751](https://github.com/user-attachments/assets/a0f7a44e-8794-4eb3-90dd-f26747232a93)





egrep '(^hello)' newfile 
## OUTPUT
![Screenshot 2025-05-21 212820](https://github.com/user-attachments/assets/948111cc-8e2e-4bec-8c48-30649d4681a0)




egrep '(world$)' newfile 
## OUTPUT
![Screenshot 2025-05-21 212848](https://github.com/user-attachments/assets/69aeace5-6c52-40de-bb5d-2c0a7bcd20b8)




egrep '(World$)' newfile 
## OUTPUT
![Screenshot 2025-05-21 213225](https://github.com/user-attachments/assets/9d543b83-3f22-4f50-9f9f-805588e2ea12)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot 2025-05-21 213321](https://github.com/user-attachments/assets/cc231b6c-6587-4606-bf0c-529c22e046cf)





egrep '[1-9]' newfile 
## OUTPUT
![Screenshot 2025-05-21 213351](https://github.com/user-attachments/assets/0fc73f94-bf9d-4d63-a71e-eb7615bbdd5d)




egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot 2025-05-21 213430](https://github.com/user-attachments/assets/3b1b63c4-ef1f-4b7a-995a-4abb8a75f4d0)



egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2025-05-21 214020](https://github.com/user-attachments/assets/7ff74ec0-a30d-4012-bc3f-508706706faa)



egrep l{2} newfile
## OUTPUT
![Screenshot 2025-05-21 214120](https://github.com/user-attachments/assets/e3c56411-f7ad-4f69-9aaf-9ecdfbada736)




egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2025-05-21 214215](https://github.com/user-attachments/assets/e340dc85-5014-45c4-b548-941caa4e21f3)



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
![Screenshot 2025-05-21 214427](https://github.com/user-attachments/assets/cbcdf59d-9d90-4427-bbb1-f78fe7a1ccba)




sed -n -e '$p' file23
## OUTPUT
![Screenshot 2025-05-21 214557](https://github.com/user-attachments/assets/7492947d-ccb8-40e9-85c3-68d42810a0c4)




sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-05-21 214658](https://github.com/user-attachments/assets/1a1c8292-6ed9-405c-9a2d-d05f9bb3fd39)




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-05-21 214736](https://github.com/user-attachments/assets/1c10b17a-9f2d-4319-a780-3e9a68612f81)




sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot 2025-05-21 214830](https://github.com/user-attachments/assets/8b06f98b-ecc1-41b6-a1d3-dbfdb7904fb0)




sed -n -e '1,5p' file23
## OUTPUT
![Screenshot 2025-05-21 215338](https://github.com/user-attachments/assets/8b0058fa-d7ba-4cbf-ac38-79661536b1ef)




sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot 2025-05-21 215409](https://github.com/user-attachments/assets/27823cd1-bb19-4ba9-8d12-64d5619324a5)





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot 2025-05-21 215437](https://github.com/user-attachments/assets/18394db8-1400-4961-a2b2-c032b659bbe3)




seq 10 
## OUTPUT
![Screenshot 2025-05-21 215507](https://github.com/user-attachments/assets/f0a794de-afb6-4f34-802f-5fce84c43df5)




seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot 2025-05-21 215601](https://github.com/user-attachments/assets/59812c15-e3d2-4ae4-b2c2-9d39208e08f8)




seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot 2025-05-21 215622](https://github.com/user-attachments/assets/92818f56-cb80-4960-8ca9-ed37ff619644)




seq 3 | sed '2a hello'
## OUTPUT
![Screenshot 2025-05-21 215653](https://github.com/user-attachments/assets/61dd7c76-003d-49ee-a8f7-9ea4ab1acec1)




seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2025-05-21 215716](https://github.com/user-attachments/assets/9b44602f-4003-4d58-ac5f-d63bf65cf135)



seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot 2025-05-21 215748](https://github.com/user-attachments/assets/5c97090e-e2ab-4f5f-a248-a8fc27e956a9)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot 2025-05-21 215817](https://github.com/user-attachments/assets/941fe914-578a-4944-803c-ee38ac5cdfcc)




sed -n '2,4{s/$/*/;p}' file23
![Screenshot 2025-05-21 215852](https://github.com/user-attachments/assets/f9894cf5-aeba-468b-9ed1-9da14c1a8bae)



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
![Screenshot 2025-05-21 215924](https://github.com/user-attachments/assets/87462097-3d05-4a6a-a429-37d3c4392144)



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
![Screenshot 2025-05-21 220011](https://github.com/user-attachments/assets/13151417-17cc-4be0-9d05-2cf86e6bfa77)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![Screenshot 2025-05-21 220059](https://github.com/user-attachments/assets/eb1f01a6-e867-428e-9f5d-470e704a049d)


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
 ![Screenshot 2025-05-21 220201](https://github.com/user-attachments/assets/3b79a40e-3033-476f-a963-d3270a30960f)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot 2025-05-21 220319](https://github.com/user-attachments/assets/fc646c9a-fe75-461b-aef4-0140aad9abff)




#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot 2025-05-21 220522](https://github.com/user-attachments/assets/02e290f7-065d-4489-8efb-dd3be9f0b443)



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2025-05-21 220643](https://github.com/user-attachments/assets/0bdc0b09-bdb0-4c2f-b9e9-d3276f93e6ee)
![Screenshot 2025-05-21 220715](https://github.com/user-attachments/assets/1a6263a2-ad7e-41e5-b389-e598d2af8e72)




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
![Screenshot 2025-05-21 220822](https://github.com/user-attachments/assets/44841a51-4e17-45af-a2be-3f90cbc4ff00)



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
![Screenshot 2025-05-21 220851](https://github.com/user-attachments/assets/29f5acb4-d4bf-457a-9845-2493f66772b1)


 
ls file1
## OUTPUT
![Screenshot 2025-05-21 220955](https://github.com/user-attachments/assets/3ca3997d-5fdc-417c-9900-7b3ce2c07f57)


echo $?
## OUTPUT
![Screenshot 2025-05-21 221032](https://github.com/user-attachments/assets/bad7cd19-e2ee-463e-98f9-c4224a4a6a07)

./one
bash: ./one: Permission denied
 


 
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

![Screenshot 2025-05-21 221141](https://github.com/user-attachments/assets/882ee6bc-df09-4c0c-81a1-77bc0077a592)











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

![Screenshot 2025-05-21 221333](https://github.com/user-attachments/assets/a201e2e0-c913-42de-8d17-4b6e3683b239)


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

![Screenshot 2025-05-21 221403](https://github.com/user-attachments/assets/ded404b8-cd64-4446-a571-72d9d7af0309)




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

![Screenshot 2025-05-21 221443](https://github.com/user-attachments/assets/5d9c4450-85cb-47a0-ac14-e4f1af935616)


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

![Screenshot 2025-05-21 221520](https://github.com/user-attachments/assets/85199d65-235f-4388-9572-37073719c473)


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

![Screenshot 2025-05-21 221607](https://github.com/user-attachments/assets/84b0eae6-5d31-4ebf-8ca7-bbdb461aa753)


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

![Screenshot 2025-05-21 221640](https://github.com/user-attachments/assets/6abe92c3-e0ab-4d4a-8bc2-6e3ee85649dc)

 
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

![Screenshot 2025-05-21 221724](https://github.com/user-attachments/assets/863aef0c-99c9-45c1-95e3-b3f5e45a228f)

 
 
 
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

![Screenshot 2025-05-21 222047](https://github.com/user-attachments/assets/8b3e2bb7-8f1a-44e0-8064-7b4e831b591e)

 
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

![Screenshot 2025-05-21 222158](https://github.com/user-attachments/assets/d97d34b5-9ca9-4b70-8451-64f2272bcfc5)


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

 ![Screenshot 2025-05-21 222158](https://github.com/user-attachments/assets/2417a8d2-f7fa-4645-b0dd-4d85534e7e73)


 
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

![Screenshot 2025-05-21 222338](https://github.com/user-attachments/assets/cbf638dc-3298-401a-ae5f-62ecaa467d21)


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

![Screenshot 2025-05-21 222407](https://github.com/user-attachments/assets/df01471b-ff18-4005-96c4-0ad6931dcf31)

 
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

![Screenshot 2025-05-21 222510](https://github.com/user-attachments/assets/392f4f83-c3da-409d-926a-d0d408acb827)






 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![Screenshot 2025-05-21 222537](https://github.com/user-attachments/assets/6c36a293-3a3e-4ac3-a1b2-109cb1c24d00)




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

 ![Screenshot 2025-05-21 222710](https://github.com/user-attachments/assets/aa5d2e34-49d8-42bb-9b4d-23c702f45333)

 
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

![Screenshot 2025-05-21 222817](https://github.com/user-attachments/assets/1331655e-4ff8-4016-b333-fa127c9c22aa)

 
 
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

![Screenshot 2025-05-21 222852](https://github.com/user-attachments/assets/95fd2349-29f2-43e1-b6ab-b0f6ac388d53)

 
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

![Screenshot 2025-05-21 222920](https://github.com/user-attachments/assets/3ea1ed1c-426a-40d6-9f5d-e91d3fc69370)



# RESULT:
The Commands are executed successfully.
