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
<img width="537" height="112" alt="image" src="https://github.com/user-attachments/assets/29fc2d95-0f1b-48ea-83c2-b853894db203" />



cat < file2
## OUTPUT
<img width="438" height="134" alt="image" src="https://github.com/user-attachments/assets/d219f8a5-7a50-4499-aebd-1afb583ff33e" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="476" height="50" alt="image" src="https://github.com/user-attachments/assets/35d02122-b11b-442a-8ca7-465af953d56f" />


comm file1 file2
 ## OUTPUT
<img width="441" height="175" alt="image" src="https://github.com/user-attachments/assets/ac07b593-3a55-4dac-ac1d-ca6b6e8b35f3" />

 
diff file1 file2
## OUTPUT
<img width="517" height="273" alt="image" src="https://github.com/user-attachments/assets/7ca8fadf-be3a-43c7-a3d7-c7ab6dbb013e" />


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
<img width="435" height="72" alt="image" src="https://github.com/user-attachments/assets/c9906e02-b216-402b-88f6-8d73f6653514" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="399" height="88" alt="image" src="https://github.com/user-attachments/assets/daaf5ac9-20ec-4fba-b0c5-cf094122805a" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="376" height="96" alt="image" src="https://github.com/user-attachments/assets/514eaef6-a6bf-4446-bffe-fc1e490ef206" />


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

<img width="344" height="49" alt="image" src="https://github.com/user-attachments/assets/1756604e-77c1-4319-a2ad-013269a70ab0" />


grep hello newfile 
## OUTPUT
<img width="398" height="52" alt="image" src="https://github.com/user-attachments/assets/c64b085d-8950-4e6c-8b34-1c2cdcc57bcf" />




grep -v hello newfile 
## OUTPUT

<img width="439" height="55" alt="image" src="https://github.com/user-attachments/assets/215df8fb-3884-4574-9e5b-272570128b02" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="473" height="72" alt="image" src="https://github.com/user-attachments/assets/244cd8a7-79db-4bc3-a1eb-8f6a42e2d591" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="485" height="56" alt="image" src="https://github.com/user-attachments/assets/61d64417-8530-4d13-9c83-630c01b26d42" />



grep -R Parrot /etc
## OUTPUT
<img width="1037" height="657" alt="image" src="https://github.com/user-attachments/assets/1f88536d-1174-461f-a994-6ad794ef2dc5" />



grep -w -n world newfile   
## OUTPUT
<img width="473" height="76" alt="image" src="https://github.com/user-attachments/assets/507e77a6-0926-49a9-b2c7-949f91925b9e" />


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
<img width="470" height="74" alt="image" src="https://github.com/user-attachments/assets/bef214dd-0a99-4cf5-ba3c-d0e88639a72d" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="483" height="69" alt="image" src="https://github.com/user-attachments/assets/2cc28f13-f5c5-4c6d-9d8d-344300852986" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="531" height="74" alt="image" src="https://github.com/user-attachments/assets/0676985b-4790-4bc5-b54f-34c0aed67514" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="561" height="50" alt="image" src="https://github.com/user-attachments/assets/58bebe86-c2bc-41f6-8478-3c1cbc68fc11" />



egrep '(world$)' newfile 
## OUTPUT



egrep '(World$)' newfile 
## OUTPUT
<img width="561" height="91" alt="image" src="https://github.com/user-attachments/assets/201efc03-9e99-4c89-a25b-4ecc0ca968d9" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="492" height="96" alt="image" src="https://github.com/user-attachments/assets/286d9214-18a7-4616-8b7d-c8774eead67f" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="536" height="51" alt="image" src="https://github.com/user-attachments/assets/03d9ac32-05ce-410c-a5b5-426ad1081cb4" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="531" height="78" alt="image" src="https://github.com/user-attachments/assets/5545313e-ec93-4fa9-87d4-65802b7bd3a6" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="531" height="78" alt="image" src="https://github.com/user-attachments/assets/2e1e3f23-1197-40cd-aa23-6f92bb420fe4" />


egrep l{2} newfile
## OUTPUT
<img width="438" height="71" alt="image" src="https://github.com/user-attachments/assets/bfaf842f-cdab-4b85-9013-991cb777c227" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="477" height="96" alt="image" src="https://github.com/user-attachments/assets/8e9814c4-274f-4c77-9eb5-def38f0046da" />


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
<img width="403" height="40" alt="image" src="https://github.com/user-attachments/assets/0e19b30a-2480-44c8-84d7-b2d21522f890" />



sed -n -e '$p' file23
## OUTPUT
<img width="388" height="39" alt="image" src="https://github.com/user-attachments/assets/8629ba5c-e751-476c-90da-91f751fb0a5f" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="465" height="182" alt="image" src="https://github.com/user-attachments/assets/58632b39-1e88-4137-8839-d7ba3aaea4c4" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="517" height="207" alt="image" src="https://github.com/user-attachments/assets/7e549d32-aa5d-4945-8ca1-632adaaf029c" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="517" height="198" alt="image" src="https://github.com/user-attachments/assets/877d430a-ff79-4464-9700-e61b698c1e92" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="492" height="134" alt="image" src="https://github.com/user-attachments/assets/0d6af2c1-3437-4609-8a51-ce2948e53eec" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="492" height="180" alt="image" src="https://github.com/user-attachments/assets/15769e67-dc6a-489c-b1aa-0de8e9e25aac" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="581" height="161" alt="image" src="https://github.com/user-attachments/assets/2a6186e6-69d5-4a72-a398-15d9bd90b39f" />



seq 10 
## OUTPUT
<img width="380" height="244" alt="image" src="https://github.com/user-attachments/assets/fed00793-8425-47e0-b656-6444d4e97b3e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="465" height="93" alt="image" src="https://github.com/user-attachments/assets/c9d8303d-6075-41cb-a83e-70fa61f6d181" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="415" height="92" alt="image" src="https://github.com/user-attachments/assets/25475dfb-c1b6-416b-a595-5b6da118f3ca" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="458" height="108" alt="image" src="https://github.com/user-attachments/assets/6f5d6773-e551-4544-8c3d-647c910a02f5" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="446" height="92" alt="image" src="https://github.com/user-attachments/assets/3851fa86-b5e8-4524-9389-e405d80c5e85" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="472" height="91" alt="image" src="https://github.com/user-attachments/assets/b384d4be-d8e0-4a43-9e22-a64d61c13bb0" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="517" height="94" alt="image" src="https://github.com/user-attachments/assets/17a5ae45-4051-41ea-b1ca-832b0e5a0370" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="526" height="98" alt="image" src="https://github.com/user-attachments/assets/b932d77a-7c41-4742-9e32-c1f2740a6429" />


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
<img width="538" height="140" alt="image" src="https://github.com/user-attachments/assets/44efed6b-afdf-40d5-b68d-cd37b22aafe4" />


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
<img width="473" height="138" alt="image" src="https://github.com/user-attachments/assets/910a1596-046b-4e0b-8aae-f9c34d15e2e3" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="576" height="192" alt="image" src="https://github.com/user-attachments/assets/012f36c8-658d-46ea-be4e-1831b961de75" />

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
<img width="531" height="92" alt="image" src="https://github.com/user-attachments/assets/1d5eeb6c-6439-4815-9aab-20e75578fddb" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="575" height="91" alt="image" src="https://github.com/user-attachments/assets/d632621f-a91f-4cfe-8038-3befdb37785c" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="650" height="399" alt="image" src="https://github.com/user-attachments/assets/f3b6452f-2f9c-4f42-9c26-a02cd5d45268" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="879" height="463" alt="image" src="https://github.com/user-attachments/assets/0e4eea8b-70d2-4fd4-84a2-6355e13649ef" />


tar -xvf backup.tar
## OUTPUT
<img width="694" height="507" alt="image" src="https://github.com/user-attachments/assets/2676a9cf-1a84-4b33-8ece-96f606c5f1bd" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="811" height="98" alt="image" src="https://github.com/user-attachments/assets/6e5e7985-feff-4c55-aa63-9f1db1ce6d6c" />

gunzip backup.tar.gz
## OUTPUT
<img width="897" height="78" alt="image" src="https://github.com/user-attachments/assets/dea08c6a-e5da-44f6-ace6-dcc47b63b35a" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="828" height="96" alt="image" src="https://github.com/user-attachments/assets/b23037a7-2cfe-4167-9414-734fbfafd308" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="541" height="95" alt="image" src="https://github.com/user-attachments/assets/fb0ae748-ba85-4ffc-96f6-62323c1ee9e8" />


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

 <img width="487" height="62" alt="image" src="https://github.com/user-attachments/assets/aa316c6d-39e4-423d-aafe-24fdbade0ad6" />

ls file1
## OUTPUT
<img width="644" height="406" alt="image" src="https://github.com/user-attachments/assets/a75de1a9-af7e-4596-b376-3abba0acee9d" />

echo $?
## OUTPUT 
<img width="423" height="47" alt="image" src="https://github.com/user-attachments/assets/db0164c8-dc94-404f-877c-c02a7ae3a670" />



./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="559" height="106" alt="image" src="https://github.com/user-attachments/assets/ef872490-1cea-4bc4-b54b-fa816dfe0a8c" />

abcd
 
echo $?
 ## OUTPUT
<img width="476" height="60" alt="image" src="https://github.com/user-attachments/assets/7f8be178-6d87-4f98-927e-5b3b493686e9" />


 
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
<img width="469" height="255" alt="image" src="https://github.com/user-attachments/assets/f6326724-4bbd-410d-8efc-b274860f197c" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="636" height="135" alt="image" src="https://github.com/user-attachments/assets/e93b31b5-8f52-4edb-b05f-6e607413a7a4" />


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
<img width="637" height="128" alt="image" src="https://github.com/user-attachments/assets/08f69155-7280-4d7a-98da-c4d63ec42557" />

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
<img width="472" height="50" alt="image" src="https://github.com/user-attachments/assets/a6e44c70-5c4a-4d0f-aa4d-e6cd47671180" />



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
<img width="657" height="114" alt="image" src="https://github.com/user-attachments/assets/10fcc8e4-d8c6-4441-ac5d-bc73a2ec5452" />

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
<img width="680" height="138" alt="image" src="https://github.com/user-attachments/assets/ca1ab6df-98da-43b5-b87f-691869ea19e6" />

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
<img width="611" height="94" alt="image" src="https://github.com/user-attachments/assets/be4d2893-371d-45d7-a3ee-d61b4d6cf432" />


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
<img width="664" height="92" alt="image" src="https://github.com/user-attachments/assets/6a9f2d52-1cb5-41b1-9eb7-eeacade67b92" />

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
<img width="651" height="107" alt="image" src="https://github.com/user-attachments/assets/a3b7bbe4-81a5-4e1d-9f61-fd910e4d0833" />

 
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
<img width="634" height="334" alt="image" src="https://github.com/user-attachments/assets/c65f348c-ef06-4bdf-af4d-54defe799c1d" />

 
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
## OUTPUT
<img width="593" height="161" alt="image" src="https://github.com/user-attachments/assets/bf919d66-e231-4086-ab24-f9f6b87b9d16" />

 
 
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
 ## OUTPUT
 <img width="631" height="230" alt="image" src="https://github.com/user-attachments/assets/d960a6fc-a229-4f42-b3aa-faaff33c1c9f" />

 
cat > forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
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
## OUTPUT
<img width="641" height="162" alt="image" src="https://github.com/user-attachments/assets/c6e924cf-4b5c-41a8-9b0a-085e5ea37a68" />

 
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
<img width="717" height="117" alt="image" src="https://github.com/user-attachments/assets/6970e9af-1891-49d8-a609-d049696159ab" />


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
<img width="644" height="112" alt="image" src="https://github.com/user-attachments/assets/36e285da-e440-4b8c-a425-dd54a38eb7a4" />


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
<img width="557" height="164" alt="image" src="https://github.com/user-attachments/assets/34dac5a2-61aa-419a-b80a-a2610d1fcc21" />

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
<img width="660" height="203" alt="image" src="https://github.com/user-attachments/assets/ef459285-1caf-409b-88b0-38f58605afb1" />

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
<img width="617" height="309" alt="image" src="https://github.com/user-attachments/assets/058fa811-9a68-4c35-89dd-81b2850fc95c" />

 
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
<img width="573" height="121" alt="image" src="https://github.com/user-attachments/assets/981e5154-3cec-4e1c-b38e-ffa83c4c2773" />

 
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
 <img width="533" height="157" alt="image" src="https://github.com/user-attachments/assets/19a69f77-c433-402c-a794-c17205a48666" />

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
<img width="583" height="103" alt="image" src="https://github.com/user-attachments/assets/c6278659-88eb-43b9-bf78-cc07dd4ed48a" />

 
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
## OUTPUT
<img width="428" height="69" alt="image" src="https://github.com/user-attachments/assets/4ecab870-96b0-479c-9486-d7108ddc9a72" />


 
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
<img width="485" height="113" alt="image" src="https://github.com/user-attachments/assets/176c5c8e-546e-41f4-b71d-8618dbd6376c" />

 
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
<img width="524" height="119" alt="image" src="https://github.com/user-attachments/assets/96601f7c-b820-429a-8e61-2a8473e949f0" />

 
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
<img width="672" height="357" alt="image" src="https://github.com/user-attachments/assets/e2f3c5eb-9bcf-4977-9a09-e163a7761c66" />

 
 
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
 <img width="605" height="274" alt="image" src="https://github.com/user-attachments/assets/f135520f-b170-4652-a350-9ad4589725d4" />

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
<img width="487" height="120" alt="image" src="https://github.com/user-attachments/assets/388709d1-2445-4a31-ad4d-e676ae4df7c7" />


# RESULT:
The Commands are executed successfully.
