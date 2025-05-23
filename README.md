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
![image](https://github.com/user-attachments/assets/d9360d68-4641-40ae-a082-bf540cd822fb)



cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/6a07835b-b988-4dce-aae3-c48d33b3f4e0)



# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/5ffbf8e1-d192-4c91-8c0a-564da7017a05)




 
comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/88f0ba70-56f6-4791-80c4-9c9c69306078)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/cc82483b-9672-446b-9c0d-ce9dc26c83b0)



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
![image](https://github.com/user-attachments/assets/2f2cd5c0-2189-4bf4-b01d-b0c50786f9f4)



cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/3ac90117-50ed-48ae-8220-d6eed29613ab)




cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/fece6ccb-158b-4ea6-bbfb-040ddf130937)



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
![image](https://github.com/user-attachments/assets/4ac9a0b2-554e-425d-b64e-d02bedb47d69)


grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/054aca5a-14cd-4f1d-8a76-44f98a174d8b)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/83d8e54d-e0b2-4dd9-8eac-df2278f05f05)




cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/a3a884d7-7fa0-4719-8c6c-b674c02246fe)




cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/30e32ccd-5a72-4a17-9be1-94842a5c8fca)



grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/33f9ecef-2d95-4097-8db0-14a523ba5c2a)




grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/fd386ce8-b8ee-4877-858c-582d5571a1e3)



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
![image](https://github.com/user-attachments/assets/feeda998-82df-4779-acc9-d2ad36978b95)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/1c01ee9f-bb4f-4a9a-9fdb-32bdbd364f44)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/6ab34a99-30c7-465b-b837-25d923be4eea)



egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e6c4a489-1bcd-492f-b7a5-b6e47a33c8d0)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/50572cf5-7233-40f0-8049-ec6cbff4f987)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8acb4950-0163-4c89-95a0-2a641fa8e13d)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/c79b0c71-c2fc-4914-a8f5-2614557bbbb5)




egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e81e1122-fdee-4307-93b8-eafc932fd53e)




egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a3efeb4b-7583-488c-ad59-fca916a737eb)



egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/1c9ffec6-218d-4e09-8207-4f55608a998d)



egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/ec92c79f-1782-46ec-87cf-6ab2570c007b)




egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/e0de5a22-e6a6-4cd6-9894-322cc392f758)



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
![image](https://github.com/user-attachments/assets/226fd0e3-1dd2-426a-afbc-a23c5d9c9c4f)




sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/6adbc168-1768-4368-92f0-2298fb4b2503)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/13b686b5-1606-4b24-841e-a27f3ebbf028)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/3ac58093-cd85-4c4d-a74d-af38f4cc0aab)




sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/bd09170b-7a88-4741-a2b7-db50607bce3d)




sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/cc4181ce-0749-4005-bce5-28aa3b28afe9)




sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/7c9768ab-09ca-45b8-90b9-5f8397546a77)





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/a9bcb8c5-21fc-4eda-a351-fc9c550f7510)




seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/d7214d6a-9376-48eb-9a18-fa14d7bc1166)




seq 10 | sed -n '4,6p'
## OUTPUT
1![image](https://github.com/user-attachments/assets/224480b9-49f8-4b85-bbbe-7ba11f7d86ef)




seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/c41e44ba-947a-48c2-ac72-7e342ae4ae60)




seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/996dfaa9-6575-4ad8-b183-26a8144be1ae)




seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/3f69cd60-2175-4873-9ce5-6fc35facad78)



seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/d3e41110-e6f9-4453-81c0-d961ef577f59)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/715a3f06-9529-42b2-adec-f50df6bbfd96)




sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/2af30bb8-6793-4650-82a9-4fd2d2900223)



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
![image](https://github.com/user-attachments/assets/e0c0cbcf-5e80-4225-9b55-9ec5c47453ea)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/50fbb195-59b9-4929-968b-5bcbc39e9b60)


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
 ![image](https://github.com/user-attachments/assets/3d242f12-03f2-4cb4-af6b-491234dc133c)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/62f1bc91-3a4d-46d9-847e-8b68d0b18ae8)




#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/43ee37c4-d44d-4f70-999b-c69c41f8027a)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/28e3af2c-1c3d-4b21-a053-25e29d07ed38)



tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/211bb6b9-df1c-425f-83f2-80c33e5c5b38)


gzip backup.tar

ls .gz
## OUTPUT

 
gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/cc223a28-6990-44dd-8dd8-83fa1b6c21fa)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/cb85bb06-c6ea-49fc-978f-fd391f6ed0c5)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/70a38dc7-e1c6-466f-8022-02a28d79d1e1)



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
![image](https://github.com/user-attachments/assets/3f93fb81-1de8-4eeb-a42d-c2a75f3edf47)


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
![image](https://github.com/user-attachments/assets/cf0ab057-ba2e-4e90-9869-b91b641f4ae5)

 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/57e3543e-3a52-4850-82be-9f85dd9ee4d7)

 
abcd
 
echo $?
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/80b77f18-5bc7-48de-9102-18ecbf94dece)

 


 
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
![image](https://github.com/user-attachments/assets/3337e0c7-5118-4e56-89ad-5c3e63195f07)




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/f1d4553f-7cb2-4d04-85b2-da1879e6cf89)



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

cat ifnested.sh # check if with file location
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
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo
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
 
 ![Screenshot 2024-03-01 233203](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/7f3f4232-c556-487d-845d-36ad26360a71)

 
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
 ![Screenshot 2024-03-01 233216](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/00883fb1-6489-4163-99fc-b750d8b77ef1)

 
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
 ![Screenshot 2024-03-01 233228](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/848dac7e-3175-4701-bf4f-851386219d97)

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
 ![Screenshot 2024-03-01 233242](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/29b13d20-62ba-4b80-8206-c4222a39156f)

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
![Screenshot 2024-03-01 233216](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/ca9c03f0-7d68-4586-9a4d-74bc315f2476)



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
![Screenshot 2024-03-01 233257](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/b87b1e50-b514-47b1-a331-cb30ed9cb224)



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
![Screenshot 2024-03-01 233312](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/4f0c3e69-7c5a-4776-887e-2fcabb80c203)

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
![Screenshot 2024-03-01 233326](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/b5770276-5696-4194-ac63-87877583c233)

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
![Screenshot 2024-03-01 233340](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/8fe0ee36-6320-41e3-8fa6-0712430dcfbd)

 
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
![Screenshot 2024-03-01 233405](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/e936aa33-eb93-4f40-a02a-c6a049b62b56)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 ![Screenshot 2024-03-01 233405](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/eb338c35-92de-41f7-b849-38e992330a68)

cat forbreak.sh 
```bash
![Screenshot 2024-03-01 233435](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/c97aa5a3-8d90-4017-96a3-824b17995ef4)

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
![Screenshot 2024-03-01 233448](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/c356b6f6-e74a-42c1-9f9f-6ed4474fcbd2)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![Screenshot 2024-03-01 233501](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/6df3bd1f-1c31-40de-a208-c222cd15bbf9)


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
![Screenshot 2024-03-01 233511](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/a757a821-e021-4a27-8d50-f6574565ad67)

 
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
 ![Screenshot 2024-03-01 233522](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/405693cf-99d3-43a1-be48-e550763260de)

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
![Screenshot 2024-03-01 233532](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/74e4b687-6cc5-429b-b993-ad7db8f077f6)


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
 ![Screenshot 2024-03-01 233546](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/b13086bf-891d-40e8-953e-eb519fb98979)

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

![Screenshot 2024-03-01 233618](https://github.com/RAGULRAAJAN/OS-Linux-commands-Shell-script/assets/147473144/27199787-e397-4b51-b87d-e4736a1615fa) 
```






# RESULT:



The Commands are executed successfully.
