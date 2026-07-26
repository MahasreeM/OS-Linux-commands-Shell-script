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



seq 10 | sed -n '4,6p'
## OUTPUT



seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT



seq 2 | sed '2i hello'
## OUTPUT


seq 10 | sed '2,9c hello'
## OUTPUT


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



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



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
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
