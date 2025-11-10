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
<img width="339" height="152" alt="image" src="https://github.com/user-attachments/assets/bae81d38-6fb4-4124-9326-1ae84fe087bb" />



cat < file2
## OUTPUT
<img width="317" height="173" alt="image" src="https://github.com/user-attachments/assets/27fed866-46f4-4e2b-a7f6-fdcb8febf0c2" />




# Comparing Files
cmp file1 file2
## OUTPUT
<img width="372" height="73" alt="image" src="https://github.com/user-attachments/assets/fc47f30b-a40a-4ca6-b039-3fdfe93611a3" />


 
comm file1 file2
 ## OUTPUT
<img width="348" height="225" alt="image" src="https://github.com/user-attachments/assets/270cc12d-2474-4108-86f0-d8d387c85acf" />



 
diff file1 file2
## OUTPUT
<img width="331" height="276" alt="image" src="https://github.com/user-attachments/assets/1fe6d29c-a924-4814-9a0c-b5ce7396dfd4" />




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
<img width="315" height="99" alt="image" src="https://github.com/user-attachments/assets/98309ba3-d8e9-4534-8a63-dd094bc97e80" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="317" height="123" alt="image" src="https://github.com/user-attachments/assets/1b049f46-4075-44c8-a0ef-efe5cd178e25" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="318" height="121" alt="image" src="https://github.com/user-attachments/assets/abdbda19-afb4-4c9a-9f08-20b0c8e8fe69" />



cat > newfile 
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
<img width="318" height="75" alt="image" src="https://github.com/user-attachments/assets/8006ca74-4ed5-49dc-b45d-b976c0e96d93" />



grep hello newfile 
## OUTPUT
<img width="323" height="73" alt="image" src="https://github.com/user-attachments/assets/a63bb5b1-dbb9-4494-879a-5ed03040fead" />




grep -v hello newfile 
## OUTPUT
<img width="325" height="72" alt="image" src="https://github.com/user-attachments/assets/c05d9cc5-9bb4-4bb3-8888-5b5abcb8d612" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="360" height="96" alt="image" src="https://github.com/user-attachments/assets/9ec70746-4c3c-40a4-ba65-3bac15b999b4" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="393" height="75" alt="image" src="https://github.com/user-attachments/assets/a4536a7c-dfdb-4832-b18a-dbb29642c0dd" />




grep -R ubuntu /etc
## OUTPUT
<img width="944" height="123" alt="image" src="https://github.com/user-attachments/assets/a405e563-4de5-4ac9-a1ce-b6e7aedc7b76" />



grep -w -n world newfile   
## OUTPUT
<img width="320" height="98" alt="image" src="https://github.com/user-attachments/assets/0753b3b9-0a29-49c6-95a7-74b1a8b05593" />




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
<img width="372" height="99" alt="image" src="https://github.com/user-attachments/assets/9892ada7-562b-4060-beee-defa21d3d804" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="353" height="101" alt="image" src="https://github.com/user-attachments/assets/c8e04b76-470d-4734-b04b-9b670c75401b" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="394" height="98" alt="image" src="https://github.com/user-attachments/assets/5ab2c74a-c2ce-4250-a457-62bbf1eb7d51" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="318" height="75" alt="image" src="https://github.com/user-attachments/assets/e885a80a-c34f-442d-8370-32575e081fbd" />



egrep '(world$)' newfile 
## OUTPUT
<img width="315" height="98" alt="image" src="https://github.com/user-attachments/assets/7c215ba4-95fc-4ea4-9f7f-01e916df41f0" />



egrep '(World$)' newfile 
## OUTPUT
<img width="330" height="70" alt="image" src="https://github.com/user-attachments/assets/27dab50e-47b6-44fe-9df9-123f9f41c3a4" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="368" height="121" alt="image" src="https://github.com/user-attachments/assets/39492592-b6c2-41d3-9404-f5dcce00272f" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="318" height="75" alt="image" src="https://github.com/user-attachments/assets/3c46f261-07a1-42a3-bfaa-4cf3edcce7b6" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="354" height="74" alt="image" src="https://github.com/user-attachments/assets/da91ea7c-03b9-4827-9da4-5f343173311a" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="348" height="71" alt="image" src="https://github.com/user-attachments/assets/15932af5-e9b2-4cfc-9f87-d7dac3bb29e9" />




egrep l{2} newfile
## OUTPUT
<img width="321" height="98" alt="image" src="https://github.com/user-attachments/assets/66fc8a49-7488-405c-87ea-12332344b2b6" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="326" height="123" alt="image" src="https://github.com/user-attachments/assets/648e84a0-e3f8-4f6a-a45b-bae3268cfaaf" />




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
<img width="319" height="76" alt="image" src="https://github.com/user-attachments/assets/9a8505c9-0112-4591-8559-43544801bff4" />



sed -n -e '$p' file23
## OUTPUT
<img width="314" height="75" alt="image" src="https://github.com/user-attachments/assets/419645fa-09f2-46a4-a2b5-ee1f2ee158c5" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="354" height="252" alt="image" src="https://github.com/user-attachments/assets/efef5255-52a3-42da-9c9f-d078a38d4d7d" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="369" height="250" alt="image" src="https://github.com/user-attachments/assets/c68e3939-60a2-4059-a6ed-4feca23f7e9b" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="395" height="248" alt="image" src="https://github.com/user-attachments/assets/dd486f8a-1c63-4a72-8e27-f3aece331d26" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="329" height="176" alt="image" src="https://github.com/user-attachments/assets/c1042905-6faf-4ac0-9ecc-1602654b62a9" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="350" height="123" alt="image" src="https://github.com/user-attachments/assets/8d0c368e-24aa-4a0c-bff1-a4fe8ae217d9" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="384" height="100" alt="image" src="https://github.com/user-attachments/assets/c13c045c-ec53-4df3-8e60-aed2a922f4f8" />



seq 10 
## OUTPUT
<img width="317" height="297" alt="image" src="https://github.com/user-attachments/assets/0d05aa17-ce63-4cc4-ad19-8a5577adf768" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="318" height="123" alt="image" src="https://github.com/user-attachments/assets/16910e90-f0b2-4b24-be3c-3bfba92140a4" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="318" height="120" alt="image" src="https://github.com/user-attachments/assets/9021381c-3968-44af-b3e9-49c9c4dd8ec3" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="318" height="149" alt="image" src="https://github.com/user-attachments/assets/9ac03df2-5cf3-4936-b114-cc41fda3eb12" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="311" height="123" alt="image" src="https://github.com/user-attachments/assets/bf802a81-2e0e-490e-8127-ec24718597c4" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="326" height="119" alt="image" src="https://github.com/user-attachments/assets/e7fd48c5-9967-4391-aa8d-b76d9616f7ff" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="363" height="126" alt="image" src="https://github.com/user-attachments/assets/964f8929-ce1d-40d4-b76f-df686d23290a" />


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
<img width="335" height="175" alt="image" src="https://github.com/user-attachments/assets/7a119411-3ea4-476e-a61f-1d670abfc172" />


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
<img width="336" height="173" alt="image" src="https://github.com/user-attachments/assets/4b2b0bc5-6b49-4a81-a86d-30cd1012961b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="424" height="249" alt="image" src="https://github.com/user-attachments/assets/b9a56d12-7cf6-46be-86e3-d06a6d1cf44f" />


cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="343" height="123" alt="image" src="https://github.com/user-attachments/assets/fac59e97-13e4-4a7d-9dc0-624a8c45ec9f" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="474" height="125" alt="image" src="https://github.com/user-attachments/assets/f4a52021-6d59-4e1a-a2cf-195a694e63c5" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="333" height="249" alt="image" src="https://github.com/user-attachments/assets/5ff943cc-7b1e-4607-b497-4256749ff00f" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="619" height="250" alt="image" src="https://github.com/user-attachments/assets/ba5ea408-c5bc-463f-8688-60202ea4da42" />


tar -xvf backup.tar
## OUTPUT
<img width="424" height="249" alt="image" src="https://github.com/user-attachments/assets/f8e2b043-2473-4b3f-b258-d1270b7df838" />



gzip backup.tar

ls .gz

gunzip backup.tar.gz
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="435" height="98" alt="image" src="https://github.com/user-attachments/assets/b144942e-89c3-4df7-8c61-2c26460a32f5" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="449" height="127" alt="image" src="https://github.com/user-attachments/assets/a03de28b-545d-47d0-bf62-2c278dfffe80" />


cat > scriptest.sh 
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
<img width="619" height="447" alt="image" src="https://github.com/user-attachments/assets/fcbe484d-6395-481c-82ba-1a5dc3e11bc2" />


 
ls file1
## OUTPUT
<img width="423" height="72" alt="image" src="https://github.com/user-attachments/assets/f012eb97-9e6a-42a4-9a5a-60a72aa05405" />


echo $?
## OUTPUT 
<img width="423" height="74" alt="image" src="https://github.com/user-attachments/assets/c73e56f4-828e-4446-8a7a-43b0f0847ed0" />

 
abcd
 
echo $?
## OUTPUT
<img width="468" height="148" alt="image" src="https://github.com/user-attachments/assets/5eb4e28a-df2e-49c1-89af-c744499c9770" />


 
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
<img width="427" height="272" alt="image" src="https://github.com/user-attachments/assets/b0dbf0a2-f285-4b7f-887d-358262bc5371" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="609" height="100" alt="image" src="https://github.com/user-attachments/assets/2284344d-5db3-42dd-9368-05f3abbf063e" />


# check file ownership
cat > psswdperm.sh 
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
<img width="457" height="76" alt="image" src="https://github.com/user-attachments/assets/46be0b05-43f9-4d78-b5d6-9316a47a9283" />



# check if with file location
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
<img width="423" height="75" alt="image" src="https://github.com/user-attachments/assets/1844c946-358c-41fa-8c2c-63ef4945d28f" />



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
<img width="609" height="125" alt="image" src="https://github.com/user-attachments/assets/49fd1f69-d262-4fb3-8e01-b99f768c0f6d" />



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
<img width="633" height="150" alt="image" src="https://github.com/user-attachments/assets/319ccf34-0ad4-447e-bbb6-e28a2ac2ed69" />




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
<img width="629" height="105" alt="image" src="https://github.com/user-attachments/assets/031c5add-3e6e-4cc0-9a49-b935dec26acc" />


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
<img width="644" height="103" alt="image" src="https://github.com/user-attachments/assets/219e6655-64b0-4726-ab48-179d33d570d0" />



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
<img width="423" height="77" alt="image" src="https://github.com/user-attachments/assets/a02bc547-575c-4087-b4ee-66149884f9ce" />


 
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
$ chmod 755 whiletest
 
$ ./whiletest

## OUTPUT
<img width="441" height="304" alt="image" src="https://github.com/user-attachments/assets/79237711-8203-4c97-8392-638e94d08d49" />



 
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
$ ./untiltest.sh

## OUTPUT
<img width="504" height="175" alt="image" src="https://github.com/user-attachments/assets/4a017ee1-8dc2-417f-8ba9-0e2075e958f3" />


 
 
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
$ ./forin1.sh

## OUTPUT
<img width="603" height="249" alt="image" src="https://github.com/user-attachments/assets/329bbb47-7739-4911-89ea-1255f096fb52" />


 
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
<img width="605" height="177" alt="image" src="https://github.com/user-attachments/assets/56c4cbf4-05d4-4eed-a726-9dc1c2c4abf6" />


cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```

$ chmod 755 forin3.sh
$ ./forin3.sh 

## OUTPUT
<img width="618" height="252" alt="image" src="https://github.com/user-attachments/assets/df6a52c2-1601-4787-933e-ee70e4267a50" />


 
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
$ ./forin1.sh

## OUTPUT
<img width="615" height="252" alt="image" src="https://github.com/user-attachments/assets/7372a389-0ce8-449f-97d7-6ed8a82a5893" />



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
<img width="417" height="223" alt="image" src="https://github.com/user-attachments/assets/1436bf04-0cd0-4fdb-8e84-fa55e359fd40" />


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
<img width="422" height="175" alt="image" src="https://github.com/user-attachments/assets/42475008-5c1e-49ee-8624-0708580a9e77" />



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
<img width="428" height="76" alt="image" src="https://github.com/user-attachments/assets/cdddea3b-89be-4092-8f86-480bc44d4213" />



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
<img width="414" height="353" alt="image" src="https://github.com/user-attachments/assets/a78aec15-5751-4c48-ace5-1e78abc0d4d9" />

 
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
<img width="702" height="127" alt="image" src="https://github.com/user-attachments/assets/afba1743-02b7-4967-9a09-908c299e7760" />


cat forcontinue.sh 
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
<img width="435" height="147" alt="image" src="https://github.com/user-attachments/assets/68bae45d-fe6f-4d05-9989-f79300800260" />


 
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
<img width="442" height="100" alt="image" src="https://github.com/user-attachments/assets/0ef44a1d-0002-429f-917a-20806d1155d0" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. "
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 


## OUTPUT
<img width="451" height="101" alt="image" src="https://github.com/user-attachments/assets/524573b5-f62b-400b-a24f-78219c6602f5" />


 
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
<img width="423" height="74" alt="image" src="https://github.com/user-attachments/assets/369a8ca5-0786-4c58-8d69-04272ac8fc4b" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

$ ./argshift.sh 1 2 3
## OUTPUT
<img width="420" height="124" alt="image" src="https://github.com/user-attachments/assets/b3dc6c67-0f17-4f55-aef8-d62e2194d2ff" />


 
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

$ ./argshift.sh 1 2 3
## OUTPUT
<img width="419" height="124" alt="image" src="https://github.com/user-attachments/assets/2f4797aa-917c-4736-915b-61095d21fa1e" />


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

 ./argshift.sh 1 2 3
## OUTPUT
<img width="418" height="401" alt="image" src="https://github.com/user-attachments/assets/7d2af3b7-78f9-433a-b67c-14633bf26e8f" />

 
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
<img width="444" height="373" alt="image" src="https://github.com/user-attachments/assets/d5a27bc0-8e4a-4ad7-b6c1-8b68ddae8bb5" />


 
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
<img width="433" height="126" alt="image" src="https://github.com/user-attachments/assets/cdfd2ebe-5e0a-438e-89f6-d52db6af51f9" />


# RESULT:
The Commands are executed successfully.
