
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
<img width="350" height="160" alt="image" src="https://github.com/user-attachments/assets/234d4284-bbf4-4098-986e-37edd813e8ed" />



cat < file2
## OUTPUT
<img width="323" height="185" alt="image" src="https://github.com/user-attachments/assets/a1ed7ca4-67be-4a57-aa7c-a0e256ac8007" />



# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="613" height="82" alt="Screenshot 2026-04-27 223322" src="https://github.com/user-attachments/assets/1866b52f-3243-450e-a26d-cfbc0f978bfc" />

comm file1 file2
 ## OUTPUT
<img width="418" height="72" alt="image" src="https://github.com/user-attachments/assets/60b1c346-90b6-4f21-8639-0b1ea2d4e110" />


 
diff file1 file2
## OUTPUT
<img width="404" height="273" alt="image" src="https://github.com/user-attachments/assets/b3f5c0a5-1947-46c5-b125-3c5e35d4fd22" />


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
<img width="365" height="104" alt="image" src="https://github.com/user-attachments/assets/d1a02fc8-e0a5-4cc3-9b0e-2a67316acd5c" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="413" height="135" alt="image" src="https://github.com/user-attachments/assets/fd798c6f-6ee5-439c-955e-71329f312894" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="354" height="133" alt="image" src="https://github.com/user-attachments/assets/7bf0cf5e-7c78-42a0-bdf0-0f92687f0c97" />


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
<img width="363" height="78" alt="image" src="https://github.com/user-attachments/assets/4db6279b-bb6d-48eb-aa5e-72efb1372f31" />



grep hello newfile 
## OUTPUT
<img width="322" height="82" alt="image" src="https://github.com/user-attachments/assets/5fc0983f-94c2-41db-b447-80271505e29a" />




grep -v hello newfile 
## OUTPUT
<img width="328" height="72" alt="image" src="https://github.com/user-attachments/assets/03a26403-f66d-4202-ab24-8f0fe389abea" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="367" height="101" alt="image" src="https://github.com/user-attachments/assets/ca331572-71c0-48b8-a22b-b25d02b15948" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="408" height="81" alt="image" src="https://github.com/user-attachments/assets/c56d7213-752f-4b4a-ab85-2b51b0eae34d" />




grep -R ubuntu /etc
## OUTPUT
<img width="633" height="413" alt="image" src="https://github.com/user-attachments/assets/dd05f5e1-5751-4c8f-8d36-f92585080e32" />



grep -w -n world newfile   
## OUTPUT
<img width="352" height="111" alt="image" src="https://github.com/user-attachments/assets/4bec944c-d79d-4044-8c61-958b94d5c915" />


cat  newfile 
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
<img width="434" height="108" alt="image" src="https://github.com/user-attachments/assets/ffe8c33a-b43f-48c7-abfc-38c0c48251dd" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="364" height="87" alt="image" src="https://github.com/user-attachments/assets/11b08fb0-d3dd-46cd-a473-f90f45050e23" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="414" height="102" alt="image" src="https://github.com/user-attachments/assets/3dec9a30-06d2-4a39-af84-a4e5098c009b" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="328" height="84" alt="image" src="https://github.com/user-attachments/assets/a3a331ab-9fb9-4c59-a8a0-126aa55eae77" />



egrep '(world$)' newfile 
## OUTPUT
<img width="336" height="109" alt="image" src="https://github.com/user-attachments/assets/b2080877-d28c-4403-99c7-24fe37a80004" />



egrep '(World$)' newfile 
## OUTPUT
<img width="341" height="81" alt="image" src="https://github.com/user-attachments/assets/a79650dc-f87e-44a9-a08b-c95e3758eb53" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="383" height="131" alt="image" src="https://github.com/user-attachments/assets/336e12ed-7866-40bb-831f-5079f521120b" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="344" height="78" alt="image" src="https://github.com/user-attachments/assets/80c6a67b-64f8-4bec-b2c5-4e7aa2f9a5e7" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="392" height="80" alt="image" src="https://github.com/user-attachments/assets/a1755d3e-6678-4216-ae57-1aeebcc1cf2c" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="394" height="69" alt="image" src="https://github.com/user-attachments/assets/889bd008-59cb-4a62-a0c2-3b6057ceb559" />


egrep l{2} newfile
## OUTPUT
<img width="391" height="107" alt="image" src="https://github.com/user-attachments/assets/ae309cac-b4cd-476c-93f7-0f016ad32537" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="355" height="129" alt="image" src="https://github.com/user-attachments/assets/d26895ee-b539-4b7e-9a04-9af25890d339" />


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
<img width="387" height="92" alt="image" src="https://github.com/user-attachments/assets/c12bfed7-e3e4-4835-a101-bb1e6eebc9f5" />



sed -n -e '$p' file23
## OUTPUT
<img width="345" height="90" alt="image" src="https://github.com/user-attachments/assets/b8655d64-b105-41cb-b8ec-6c0f36cd9520" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="410" height="254" alt="image" src="https://github.com/user-attachments/assets/e1877a0b-3b11-4a9d-be85-d9ede29543e2" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="396" height="253" alt="image" src="https://github.com/user-attachments/assets/0e2afe09-06e5-4053-95a2-6b365fe44ed6" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="506" height="254" alt="image" src="https://github.com/user-attachments/assets/452a7715-20c5-4b8d-9324-4856ddc02222" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="388" height="175" alt="image" src="https://github.com/user-attachments/assets/a48df51f-e5f5-4ccd-937e-e5afce7f2560" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="379" height="133" alt="image" src="https://github.com/user-attachments/assets/8bcd3e28-00f5-4ca3-9b01-9da158f48e7d" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="427" height="99" alt="image" src="https://github.com/user-attachments/assets/abd0bb6b-6fb8-4467-9c29-de7c44ae1338" />



seq 10 
## OUTPUT
<img width="429" height="304" alt="image" src="https://github.com/user-attachments/assets/046a83dd-1b86-48dd-b119-36de7e2e8729" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="348" height="128" alt="image" src="https://github.com/user-attachments/assets/998ec0e8-6c72-454e-a64d-9f5bcd601fac" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="305" height="131" alt="image" src="https://github.com/user-attachments/assets/a8867583-4939-45dd-9474-fea9e309a89b" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="310" height="149" alt="image" src="https://github.com/user-attachments/assets/9a905f97-d919-4790-8e47-60a2446e3549" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="318" height="129" alt="image" src="https://github.com/user-attachments/assets/2a92a9d8-dda4-4d1c-ad94-f2f3edc342a4" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="315" height="124" alt="image" src="https://github.com/user-attachments/assets/b15c285b-2349-4601-9ca0-46558c67c656" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="395" height="130" alt="image" src="https://github.com/user-attachments/assets/1c986f8b-0418-4369-bcdf-4cefc77092cf" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="384" height="137" alt="image" src="https://github.com/user-attachments/assets/47b73fdf-9bfd-417f-b2d9-1edde291a453" />

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
<img width="346" height="158" alt="image" src="https://github.com/user-attachments/assets/30dd3f24-b594-4bec-aa86-5c625283f229" />


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
<img width="351" height="162" alt="image" src="https://github.com/user-attachments/assets/cf8e8303-b30c-4eca-af83-5a85b6b54772" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="454" height="242" alt="image" src="https://github.com/user-attachments/assets/0db96f57-a004-49d8-91f0-cbe030aa56b3" />

cat > urllist.txt
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
<img width="351" height="106" alt="image" src="https://github.com/user-attachments/assets/97b05d84-9e1b-44c0-ab82-c5bf7a8ef6b9" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="464" height="102" alt="image" src="https://github.com/user-attachments/assets/d3c97f81-b8bf-428f-bc43-4f8d985e57ec" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="518" height="242" alt="image" src="https://github.com/user-attachments/assets/5e1c72ef-ac15-4168-bb65-f2b3229463ff" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="565" height="449" alt="image" src="https://github.com/user-attachments/assets/53da02af-d714-469d-8443-f3a63d1761dc" />


tar -xvf backup.tar
## OUTPUT
<img width="507" height="326" alt="image" src="https://github.com/user-attachments/assets/bb3076d2-5322-474d-91c2-4c303a4c57b6" />

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
<img width="621" height="353" alt="image" src="https://github.com/user-attachments/assets/47e754b9-760a-424f-a02d-df90ad2765c0" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="321" height="140" alt="image" src="https://github.com/user-attachments/assets/732baf43-7030-41d2-afc3-38caa18466e2" />


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

cat  > scriptest.sh 
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
<img width="406" height="134" alt="image" src="https://github.com/user-attachments/assets/a1020ebd-18c0-4781-8d74-bcaae27fa95c" />

 
ls file1
## OUTPUT
<img width="331" height="78" alt="image" src="https://github.com/user-attachments/assets/44a98bbd-76d7-4d02-8ba3-0b8778a82b6c" />

echo $?
## OUTPUT
<img width="295" height="77" alt="image" src="https://github.com/user-attachments/assets/15a439ec-dffa-4aca-b094-d8ddf619d45d" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="295" height="77" alt="image" src="https://github.com/user-attachments/assets/15a439ec-dffa-4aca-b094-d8ddf619d45d" /> 
abcd
 
echo $?
 ## OUTPUT
<img width="295" height="77" alt="image" src="https://github.com/user-attachments/assets/15a439ec-dffa-4aca-b094-d8ddf619d45d" />

 
# mis-using string comparisons

cat > strcomp.sh 
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

cat > strcomp.sh 
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
<img width="420" height="129" alt="image" src="https://github.com/user-attachments/assets/103cfac8-6492-49e7-9a55-debcabb8be93" />


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
<img width="412" height="91" alt="image" src="https://github.com/user-attachments/assets/4ab8432e-356a-465d-aca9-faf4f99ec387" />

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
<img width="385" height="97" alt="image" src="https://github.com/user-attachments/assets/bbfd4ab7-b0d8-47e7-9926-eb2e96390f0b" />



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
<img width="337" height="94" alt="image" src="https://github.com/user-attachments/assets/703ce65a-5fc4-4de4-a7f8-2fdb003ee692" />


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
<img width="351" height="132" alt="image" src="https://github.com/user-attachments/assets/1e35e3ff-b091-4682-ab50-c6a6b01f69f7" />

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
<img width="420" height="442" alt="image" src="https://github.com/user-attachments/assets/dde9bbd6-97c8-4bf7-b0ba-675f0fdd83e9" />


cat > forctype.sh 
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
<img width="333" height="189" alt="image" src="https://github.com/user-attachments/assets/bb76dd5e-3101-4a80-ab05-331ee6374526" />

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
<img width="333" height="189" alt="image" src="https://github.com/user-attachments/assets/e3d3a6f6-716d-4c67-ba7b-468446f8f5e7" />

 
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

 
cat > exread.sh 
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
<img width="532" height="209" alt="image" src="https://github.com/user-attachments/assets/51f44dc6-bca0-4de7-8a70-d2092ca3d2e5" />



# RESULT:
The Commands are executed successfully.
