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
<img width="807" height="152" alt="image" src="https://github.com/user-attachments/assets/07621aaa-b55c-41ec-9d1e-4deb7d67513b" />



cat < file2
## OUTPUT
<img width="827" height="173" alt="image" src="https://github.com/user-attachments/assets/21c0d317-f247-4d8e-b4f5-0d706d718a7e" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="710" height="72" alt="image" src="https://github.com/user-attachments/assets/42c01abd-33a9-4724-9721-d9a27164fcda" />


comm file1 file2
 ## OUTPUT
<img width="723" height="222" alt="image" src="https://github.com/user-attachments/assets/0ac22afc-e62e-4d26-b052-529fba389659" />

 
diff file1 file2
## OUTPUT
<img width="785" height="276" alt="image" src="https://github.com/user-attachments/assets/6a3badc4-d325-41ae-a891-f07313ba279d" />


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
<img width="955" height="220" alt="image" src="https://github.com/user-attachments/assets/c0784f29-948a-4866-aa32-92fa148fd38c" />


cut -c1-3 file11
## OUTPUT

<img width="965" height="107" alt="image" src="https://github.com/user-attachments/assets/8e0cc4b0-7f36-44bd-ba80-3a30cfebcf65" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="698" height="128" alt="image" src="https://github.com/user-attachments/assets/6c720080-56ad-4a71-b00f-a9e4b1eef2c4" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="647" height="127" alt="image" src="https://github.com/user-attachments/assets/2a1d0b04-a77d-4b88-9c8d-2e6642006c68" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
<img width="688" height="201" alt="image" src="https://github.com/user-attachments/assets/61cfb848-93d8-4f9a-91fe-1e372edf86f2" />
 
grep Hello newfile 
## OUTPUT

<img width="657" height="77" alt="image" src="https://github.com/user-attachments/assets/7eda50ab-2fd7-487d-8778-bfe0072b033b" />


grep hello newfile 
## OUTPUT

<img width="640" height="75" alt="image" src="https://github.com/user-attachments/assets/ac5d7f5a-829e-4b2b-b5f2-a2b826671e27" />



grep -v hello newfile 
## OUTPUT

<img width="678" height="73" alt="image" src="https://github.com/user-attachments/assets/fd1793a1-c34d-48a1-a815-013233244715" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="666" height="103" alt="image" src="https://github.com/user-attachments/assets/99e23d18-e976-4cbf-8092-6e848a6040d1" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="661" height="77" alt="image" src="https://github.com/user-attachments/assets/59fd843f-c903-4b11-9f54-889b124cf513" />



grep -R ubuntu /etc
## OUTPUT

<img width="1427" height="847" alt="image" src="https://github.com/user-attachments/assets/9a789e3a-3ee7-49a1-a0e0-9c961972cf57" />


grep -w -n world newfile   
## OUTPUT

<img width="706" height="97" alt="image" src="https://github.com/user-attachments/assets/8c1e69ce-d446-43e2-9b81-64f46e7e1750" />

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
<img width="697" height="352" alt="image" src="https://github.com/user-attachments/assets/f44ce948-7175-4ce0-872b-5433497f34f3" />

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

<img width="642" height="102" alt="image" src="https://github.com/user-attachments/assets/db1578c5-8a81-40f7-bc37-3f9dd24b36ea" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="672" height="97" alt="image" src="https://github.com/user-attachments/assets/eba67705-a7c8-4034-902b-e823a0431d88" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="648" height="98" alt="image" src="https://github.com/user-attachments/assets/812cdc68-a3c0-422b-beb9-90aa713d19e4" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="697" height="72" alt="image" src="https://github.com/user-attachments/assets/8db097a7-e729-448a-905c-58dab1e7d55d" />


egrep '(world$)' newfile 
## OUTPUT
<img width="646" height="97" alt="image" src="https://github.com/user-attachments/assets/d7b9801b-4543-4d8b-b63c-bf91794a533e" />



egrep '(World$)' newfile 
## OUTPUT

<img width="658" height="73" alt="image" src="https://github.com/user-attachments/assets/5da49bd1-7d3d-4753-948a-f61a6bd15626" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="688" height="130" alt="image" src="https://github.com/user-attachments/assets/a7519927-1c83-49a5-8a54-f6e894849e5c" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="737" height="77" alt="image" src="https://github.com/user-attachments/assets/ba540f70-e767-4c8a-b390-3f52c374741f" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="647" height="76" alt="image" src="https://github.com/user-attachments/assets/97bfffcf-0273-47af-b2f7-264c33ba50ec" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="670" height="77" alt="image" src="https://github.com/user-attachments/assets/59a56238-e67d-427e-bdf6-c232d6e5628b" />

egrep l{2} newfile
## OUTPUT

<img width="653" height="98" alt="image" src="https://github.com/user-attachments/assets/21d849f5-2847-4fcd-afde-b5573f13c45f" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="657" height="125" alt="image" src="https://github.com/user-attachments/assets/b2ba03ec-0260-419b-b333-88c9f17e1bc3" />

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
<img width="705" height="247" alt="image" src="https://github.com/user-attachments/assets/61a74a2f-7151-4e3c-b048-3754aec88f00" />


sed -n -e '3p' file23
## OUTPUT

<img width="678" height="77" alt="image" src="https://github.com/user-attachments/assets/51b97b8e-0a2e-4adf-9264-3bb59d97a608" />


sed -n -e '$p' file23
## OUTPUT

<img width="707" height="75" alt="image" src="https://github.com/user-attachments/assets/e6560e16-dc85-4349-8445-d401ca5203fb" />

<img width="758" height="157" alt="image" src="https://github.com/user-attachments/assets/9def57bc-a377-423d-809e-533ccd48d1a0" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="702" height="250" alt="image" src="https://github.com/user-attachments/assets/81e94b4a-6ff0-4294-a2f3-2ebdd93a58ba" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="673" height="252" alt="image" src="https://github.com/user-attachments/assets/8029aaee-cc6a-4a07-ad4d-debd9c6f14f7" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="690" height="250" alt="image" src="https://github.com/user-attachments/assets/19319d52-f39f-4e8e-8fd0-d1712623e704" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="675" height="176" alt="image" src="https://github.com/user-attachments/assets/38d7408b-3d1d-4c6a-b277-4b8cad0b72f2" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="698" height="125" alt="image" src="https://github.com/user-attachments/assets/fb226c17-9a48-4a2f-8e29-0de987b6f29e" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="660" height="100" alt="image" src="https://github.com/user-attachments/assets/4a091e32-7d80-4571-a63c-b66da0d0b3ec" />


seq 10 
## OUTPUT

<img width="707" height="302" alt="image" src="https://github.com/user-attachments/assets/fa87389a-c9b4-42e9-a412-614f1e647aa3" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="735" height="132" alt="image" src="https://github.com/user-attachments/assets/8e8cc760-fdae-43b0-9cdd-d950177efed8" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="665" height="133" alt="image" src="https://github.com/user-attachments/assets/4977bb14-3336-49e8-abc7-e74b8dde058e" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="650" height="150" alt="image" src="https://github.com/user-attachments/assets/c136c654-86e4-4c39-976c-19522221f0a1" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="656" height="127" alt="image" src="https://github.com/user-attachments/assets/c5f1f32a-954c-49e1-8be5-7eb26b8c34cf" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="655" height="128" alt="image" src="https://github.com/user-attachments/assets/b4724b16-8875-4823-92a9-d59b5fabe515" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="665" height="133" alt="image" src="https://github.com/user-attachments/assets/6027868b-e12e-4695-b003-af2e70454e7f" />


sed -n '2,4{s/$/*/;p}' file23
<img width="665" height="132" alt="image" src="https://github.com/user-attachments/assets/4af524b3-e186-4b0f-904b-f785ea0976ce" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
<img width="686" height="180" alt="image" src="https://github.com/user-attachments/assets/e0fa9912-491a-4b05-9d54-07e7c7417816" />

sort file21
## OUTPUT
<img width="657" height="178" alt="image" src="https://github.com/user-attachments/assets/1a0abb29-d35f-4e25-907d-dc9a24f11a9e" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

<img width="672" height="207" alt="image" src="https://github.com/user-attachments/assets/f4cc7b9e-77fb-4f74-9abe-f9c9ae13cfa8" />

uniq file22
## OUTPUT
<img width="656" height="177" alt="image" src="https://github.com/user-attachments/assets/a7bed486-1685-451b-8649-68ff42641ea2" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="670" height="252" alt="image" src="https://github.com/user-attachments/assets/11ecc323-5d1b-4ae9-a4b6-b49e07240779" />

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

<img width="665" height="247" alt="image" src="https://github.com/user-attachments/assets/d569480a-ce66-4e65-b0ab-049d4c848e38" />

cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="647" height="131" alt="image" src="https://github.com/user-attachments/assets/6031e7ce-4c0d-46a6-b2b4-63adcf64338c" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="671" height="128" alt="image" src="https://github.com/user-attachments/assets/feaf6c96-3f9d-49fe-a65c-263e0d6c8308" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="695" height="316" alt="image" src="https://github.com/user-attachments/assets/ebd90963-c4de-4772-b5aa-6801f1f6f158" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="792" height="483" alt="image" src="https://github.com/user-attachments/assets/b85a9866-0513-4575-be13-e29c1277dc0d" />


tar -xvf backup.tar
## OUTPUT
<img width="765" height="330" alt="image" src="https://github.com/user-attachments/assets/1444c045-3fdc-46e2-bbd1-d12bebcbe957" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="757" height="127" alt="image" src="https://github.com/user-attachments/assets/55e369ea-e242-4ac2-a22e-fa554c2087b9" />

gunzip backup.tar.gz
## OUTPUT
<img width="776" height="55" alt="image" src="https://github.com/user-attachments/assets/5e277d29-b356-4631-a9b5-4e2b89d4e2a9" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="743" height="230" alt="image" src="https://github.com/user-attachments/assets/9f97dcea-e34c-486a-949e-f25dea2b5c0a" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="760" height="272" alt="image" src="https://github.com/user-attachments/assets/325631e2-ea0b-425b-950b-a150e54f58bf" />


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
<img width="756" height="328" alt="image" src="https://github.com/user-attachments/assets/e00f895c-1358-459a-91b1-5e5d2daeb58c" />

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
 <img width="753" height="322" alt="image" src="https://github.com/user-attachments/assets/d81636cb-3f3f-4d35-b9ad-8765a2d31423" />

chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="752" height="422" alt="image" src="https://github.com/user-attachments/assets/4954b3e4-ebca-4b55-a343-075e118e6455" />

 
ls file1
## OUTPUT
<img width="737" height="75" alt="image" src="https://github.com/user-attachments/assets/d5a30769-f7dd-4dfc-b5af-71bf2d399002" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="781" height="77" alt="image" src="https://github.com/user-attachments/assets/55a2696c-c76f-4e91-b124-6f54a54116f4" />

abcd
 
echo $?
 ## OUTPUT

<img width="782" height="71" alt="image" src="https://github.com/user-attachments/assets/2f9f1740-4736-4a48-92a6-5e3619af522b" />

 
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

<img width="753" height="281" alt="image" src="https://github.com/user-attachments/assets/cb1b7545-7c35-42f9-a361-34df9aa53ba2" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="742" height="127" alt="image" src="https://github.com/user-attachments/assets/bd40cc82-899d-4e85-a343-44cb4506afba" />

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
<img width="752" height="222" alt="image" src="https://github.com/user-attachments/assets/26a5e8d7-16e6-4aab-9a4f-f5da94a635b9" />

./psswdperm.sh
## OUTPUT
<img width="760" height="77" alt="image" src="https://github.com/user-attachments/assets/df241a2b-e3fe-46a5-9ec9-1e1c1e7c279f" />


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

<img width="781" height="85" alt="image" src="https://github.com/user-attachments/assets/d73da885-d993-48c2-be88-de20b13e26ab" />



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
<img width="746" height="102" alt="image" src="https://github.com/user-attachments/assets/4ce46be5-0174-4da1-9c08-220029cfb6bb" />

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
<img width="758" height="106" alt="image" src="https://github.com/user-attachments/assets/427978aa-95b7-4ca1-a24a-df1a35e9671b" />

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

<img width="750" height="80" alt="image" src="https://github.com/user-attachments/assets/ac7d4464-5798-42ec-ad8e-d9f20dfe6afa" />

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
<img width="762" height="126" alt="image" src="https://github.com/user-attachments/assets/3198b58d-a213-4b7e-a37a-9c27eca464e7" />

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
<img width="748" height="127" alt="image" src="https://github.com/user-attachments/assets/2713ba31-647e-4ce0-9c29-f7a0986dfabb" />
 
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
 
 <img width="758" height="301" alt="image" src="https://github.com/user-attachments/assets/382675f1-856e-42d9-a610-0ba4078cf90d" />

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
 
 <img width="752" height="188" alt="image" src="https://github.com/user-attachments/assets/68dd60cb-7d89-4574-97ba-211723f54c9f" />

 
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
 
<img width="747" height="202" alt="image" src="https://github.com/user-attachments/assets/984ce9ed-ffff-4007-b7ce-c029d9fe72a8" />
 
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

<img width="767" height="175" alt="image" src="https://github.com/user-attachments/assets/24bd4859-d7cf-445d-8c6f-1bb08a0355bd" />

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

<img width="737" height="253" alt="image" src="https://github.com/user-attachments/assets/d99d5d6f-fcd8-4f81-8891-fc68b5f0b745" />
 
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
<img width="773" height="457" alt="image" src="https://github.com/user-attachments/assets/a6ebd893-527d-430f-96fd-86210fee1085" />

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

<img width="752" height="227" alt="image" src="https://github.com/user-attachments/assets/eed30ac8-4d8c-41b1-a438-a8afb73a529a" />

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
<img width="753" height="185" alt="image" src="https://github.com/user-attachments/assets/02e1f12c-cc1f-43bd-a21e-c889e0c78e46" />

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

<img width="767" height="358" alt="image" src="https://github.com/user-attachments/assets/31d2e00f-5871-41d1-8032-587968fb6cfb" />
 
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
<img width="742" height="130" alt="image" src="https://github.com/user-attachments/assets/097807ad-211f-43ff-8a68-96d40501c766" />

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
<img width="758" height="180" alt="image" src="https://github.com/user-attachments/assets/236cf5de-ac40-47b4-a407-0bc3db513edb" />
 
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
<img width="746" height="98" alt="image" src="https://github.com/user-attachments/assets/de386f44-a3bb-4ef6-a2ba-78d1080fc4cf" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="751" height="106" alt="image" src="https://github.com/user-attachments/assets/b628ab0d-55b3-4d04-86ad-518b80dd56a1" />


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

 <img width="763" height="80" alt="image" src="https://github.com/user-attachments/assets/dd49871b-8299-4f70-844b-9d95c1b57145" />

 ./funcex.sh 1 2
 
<img width="777" height="87" alt="image" src="https://github.com/user-attachments/assets/4723d6ec-eb32-4ecf-9241-201cffd910c4" />

 
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

<img width="745" height="130" alt="image" src="https://github.com/user-attachments/assets/68571865-ad0d-4cb2-9a4d-870ec374d901" />
 
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
 
 <img width="781" height="397" alt="image" src="https://github.com/user-attachments/assets/ed6ca868-36ae-4d39-8b49-adf317148d73" />

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

<img width="761" height="372" alt="image" src="https://github.com/user-attachments/assets/d1590dd3-d934-4a86-9ab7-25805796baa6" />
 
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

<img width="780" height="127" alt="image" src="https://github.com/user-attachments/assets/179ebbed-85fe-4169-8819-69db1ff6c59c" />


# RESULT:
The Commands are executed successfully.
