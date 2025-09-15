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
<img width="316" height="118" alt="Screenshot from 2025-09-13 20-02-19" src="https://github.com/user-attachments/assets/97049908-7b96-44c5-8ddf-3e11289bb79d" />

cat < file2
## OUTPUT
<img width="331" height="131" alt="Screenshot from 2025-09-13 20-04-04" src="https://github.com/user-attachments/assets/e7f4c21f-d8c4-4725-9c7a-c18d6edf214d" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="347" height="51" alt="Screenshot from 2025-09-13 20-07-06" src="https://github.com/user-attachments/assets/43f46139-67f2-4c99-b98a-e53f5e09ec82" />

comm file1 file2
 ## OUTPUT
<img width="343" height="243" alt="Screenshot from 2025-09-13 20-24-11" src="https://github.com/user-attachments/assets/747b782d-f35d-476c-b86a-98ae46539fc2" />

 
diff file1 file2
## OUTPUT
<img width="338" height="183" alt="Screenshot from 2025-09-13 20-25-25" src="https://github.com/user-attachments/assets/3d059589-6804-46fd-9e89-8ab2bcff8d98" />


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

<img width="382" height="67" alt="Screenshot from 2025-09-13 20-31-47" src="https://github.com/user-attachments/assets/e4c8a1e1-ad6c-4c4b-b932-8161b23cf17a" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="406" height="88" alt="Screenshot from 2025-09-13 20-35-38" src="https://github.com/user-attachments/assets/33e05ad4-77b1-4e71-aa18-6b341cee67bb" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="406" height="88" alt="Screenshot from 2025-09-13 20-33-56" src="https://github.com/user-attachments/assets/2f9cfd9b-fea9-495f-b10a-de54b7438caa" />


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
<img width="497" height="68" alt="Screenshot from 2025-09-13 20-56-06" src="https://github.com/user-attachments/assets/8290fd3b-6632-4c33-b839-324fdd99b8b5" />




egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="473" height="86" alt="Screenshot from 2025-09-13 20-54-54" src="https://github.com/user-attachments/assets/1bdb22d8-918b-4f15-bf10-f92bce6a72c4" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="497" height="68" alt="Screenshot from 2025-09-13 20-57-54" src="https://github.com/user-attachments/assets/2ea7b4ea-18ed-44c8-9205-54ea0dff00dd" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="503" height="50" alt="Screenshot from 2025-09-13 20-59-15" src="https://github.com/user-attachments/assets/67ac3aa5-8e97-4be9-81f8-344ddba0b843" />



egrep '(world$)' newfile 
## OUTPUT
<img width="502" height="85" alt="Screenshot from 2025-09-13 21-01-46" src="https://github.com/user-attachments/assets/bb35b65b-9cec-40bd-bf74-cb97a8aeb3df" />


egrep '(World$)' newfile 
## OUTPUT
<img width="502" height="85" alt="Screenshot from 2025-09-13 21-03-55" src="https://github.com/user-attachments/assets/a485eee8-099b-4f28-89db-de18e4736387" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="502" height="86" alt="Screenshot from 2025-09-13 21-05-26" src="https://github.com/user-attachments/assets/7fe08a3f-5bd8-4150-9173-de9328e812dd" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="500" height="46" alt="Screenshot from 2025-09-13 21-06-38" src="https://github.com/user-attachments/assets/db543acc-6ebb-4e01-9dd4-04d4aadf855c" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="503" height="66" alt="Screenshot from 2025-09-13 21-07-42" src="https://github.com/user-attachments/assets/8576fa34-231a-4198-a7e3-57353a0eec8d" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="492" height="88" alt="Screenshot from 2025-09-13 21-17-28" src="https://github.com/user-attachments/assets/1544b199-2334-4421-8a18-4c2998b2b441" />


egrep l{2} newfile
## OUTPUT
<img width="503" height="66" alt="Screenshot from 2025-09-13 21-14-42" src="https://github.com/user-attachments/assets/22ed8959-8c34-4d6b-b302-9bb5ddf07a5f" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="492" height="88" alt="Screenshot from 2025-09-13 21-15-29" src="https://github.com/user-attachments/assets/8363b64d-5701-4f52-a89a-1958ff330aaf" />


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
<img width="490" height="245" alt="Screenshot from 2025-09-13 22-34-37" src="https://github.com/user-attachments/assets/c68e683d-dae0-4129-9c90-cfca602b1cac" />



sed -n -e '$p' file23
## OUTPUT


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="487" height="194" alt="Screenshot from 2025-09-13 22-43-24" src="https://github.com/user-attachments/assets/567b0191-f77d-463a-b991-06e8846be691" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="487" height="194" alt="Screenshot from 2025-09-13 22-46-16" src="https://github.com/user-attachments/assets/f895d94f-c909-4725-9537-7b0e14ae1551" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="487" height="194" alt="Screenshot from 2025-09-13 22-46-16" src="https://github.com/user-attachments/assets/e24d5eed-8c2c-4db5-8153-1dca36b67ea4" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="494" height="120" alt="Screenshot from 2025-09-13 22-47-17" src="https://github.com/user-attachments/assets/a6926bfe-af8f-4229-81b5-560708150a83" />

sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="490" height="89" alt="Screenshot from 2025-09-13 22-48-12" src="https://github.com/user-attachments/assets/8a9a81c4-30d8-414a-9db1-a59787b7fcd1" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="486" height="71" alt="Screenshot from 2025-09-13 22-51-16" src="https://github.com/user-attachments/assets/4ab2c80a-f734-44ba-b2c1-dd69793d75be" />


seq 10 
## OUTPUT

<img width="492" height="217" alt="Screenshot from 2025-09-13 22-59-48" src="https://github.com/user-attachments/assets/6288ddec-e597-4423-b4b0-af4eddc880de" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="485" height="104" alt="Screenshot from 2025-09-13 23-10-25" src="https://github.com/user-attachments/assets/201a8dfe-c341-4f83-be55-1b884711dad6" />

seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="485" height="104" alt="Screenshot from 2025-09-13 23-16-25" src="https://github.com/user-attachments/assets/13535b6d-3254-4429-bab7-a0a4740e97cb" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="485" height="104" alt="Screenshot from 2025-09-13 23-18-41" src="https://github.com/user-attachments/assets/a4188cfe-3978-47ca-81a3-c6216d6957f9" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="485" height="104" alt="Screenshot from 2025-09-13 23-20-27" src="https://github.com/user-attachments/assets/84a01552-4533-4451-9c1a-1d7c9de98d63" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="485" height="104" alt="Screenshot from 2025-09-13 23-22-02" src="https://github.com/user-attachments/assets/1b20b6a7-618d-40b6-82be-95cf621b8f74" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="485" height="104" alt="Screenshot from 2025-09-13 23-23-44" src="https://github.com/user-attachments/assets/84578be8-ebaf-4207-b7fd-4efc57aa65f9" />

sed -n '2,4{s/$/*/;p}' file23


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
<img width="447" height="265" alt="Screenshot from 2025-09-13 23-32-23" src="https://github.com/user-attachments/assets/5ae885d9-866a-480d-aac1-08d953885c54" />


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
<img width="424" height="214" alt="Screenshot from 2025-09-14 00-23-15" src="https://github.com/user-attachments/assets/abd7985e-74bb-4ac5-91e2-0851d28c831b" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="533" height="186" alt="Screenshot from 2025-09-14 00-24-35" src="https://github.com/user-attachments/assets/e6914d51-aa6e-4c51-b322-246f11e9d495" />

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

<img width="531" height="95" alt="Screenshot from 2025-09-14 00-38-01" src="https://github.com/user-attachments/assets/0195671f-30b7-4535-ab62-a51193193619" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="531" height="95" alt="Screenshot from 2025-09-14 00-35-31" src="https://github.com/user-attachments/assets/fdb89bd7-cd37-4dd7-a7d4-f0c2358add88" />

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
<img width="512" height="56" alt="Screenshot from 2025-09-14 16-20-56" src="https://github.com/user-attachments/assets/4f63d343-588e-46e7-ad6a-5697a6729f78" />


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="498" height="175" alt="Screenshot from 2025-09-14 16-28-13" src="https://github.com/user-attachments/assets/e6f52c23-cdcf-4390-8991-639950163f04" />


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
<img width="610" height="816" alt="Screenshot from 2025-09-14 16-41-12" src="https://github.com/user-attachments/assets/e5bea28b-3c1e-4809-811b-de4e0defb6e4" />

ls file1
## OUTPUT
<img width="542" height="44" alt="Screenshot from 2025-09-14 16-45-39" src="https://github.com/user-attachments/assets/dd3c4e68-34aa-4f61-8e92-7cfeb3469049" />


echo $?
## OUTPUT 

<img width="542" height="44" alt="Screenshot from 2025-09-14 16-43-52" src="https://github.com/user-attachments/assets/23fb2c04-59f1-442b-95b8-2ed2b755b01e" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT
<img width="555" height="76" alt="Screenshot from 2025-09-14 16-46-53" src="https://github.com/user-attachments/assets/f170b68b-5e4c-4358-9612-8aa176d9f8c9" />

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

chmod 755 strcomp.sh
./strcomp.sh 
## OUTPU<img width="552" height="69" alt="Screenshot from 2025-09-14 16-54-56" src="https://github.com/user-attachments/assets/80317b90-0e26-4447-9af4-9358070f8ba2" />
T


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
<img width="578" height="216" alt="Screenshot from 2025-09-14 18-11-24" src="https://github.com/user-attachments/assets/587d5f9c-d35c-4362-aa03-7f8129e51b84" />


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
<img width="438" height="409" alt="Screenshot from 2025-09-14 17-12-18" src="https://github.com/user-attachments/assets/a4a94416-d116-46e6-995b-d8de85817490" />


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
<img width="571" height="398" alt="Screenshot from 2025-09-15 20-11-31" src="https://github.com/user-attachments/assets/854a9fc2-6265-400f-873b-4e2713596eaa" />


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
<img width="438" height="409" alt="Screenshot from 2025-09-14 17-12-18" src="https://github.com/user-attachments/assets/5da4c244-04ae-48ee-b518-fa6e0e159192" />


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
<img width="630" height="460" alt="Screenshot from 2025-09-15 20-40-28" src="https://github.com/user-attachments/assets/0752fc2c-06d6-4ed0-a033-bb08f634a2bd" />


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
<img width="612" height="239" alt="Screenshot from 2025-09-15 20-44-54" src="https://github.com/user-attachments/assets/3a565402-2e22-4c3e-ab32-b05347f21c2d" />


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
<img width="612" height="296" alt="Screenshot from 2025-09-15 20-50-57" src="https://github.com/user-attachments/assets/6ce37cd0-570b-48d6-bfe8-69875c984664" />

 
$ ./whiletest.sh
 <img width="611" height="415" alt="Screenshot from 2025-09-15 20-55-14" src="https://github.com/user-attachments/assets/e0757ed4-6e83-4441-9a10-bbe38461658b" />

 
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
!
 
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
