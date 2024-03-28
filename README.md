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
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/a855ab8e-3d66-4dc3-b799-9a942b161261)



cat < file2
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/a9546ebb-50e0-487c-9bf7-f040eba81a42)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/a1ae7427-73d8-48d2-9dc9-42db5a5c37e2)
 
comm file1 file2
 ## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/b1c83744-b0f2-4188-a21a-4e9ad4d95fd5)

 
diff file1 file2
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/9cd4f477-2a63-49c3-aa2c-891fcebbc2a7)


## Filters

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
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/78bcef79-4ce7-45ff-a430-f949e55a6d77)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/bf18e9e9-5477-46ec-8263-c92a8a8be5cf)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/72b54143-2a43-4b1f-a58f-d13d98a42ab1)


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
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/a1b3fa74-2b57-467d-8e67-631505accd71)



grep hello newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/40c43b51-60ad-447d-9dca-41695a2746e2)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/2e95fad0-d77a-4113-b741-d650d2e9ec78)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/e1f5952f-f93e-4d28-88fa-d15549d9c27e)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/541fc42b-e974-4c49-acff-f66cb80781de)


grep -w -n world newfile   
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/7d2494b9-20cc-4a2b-a878-72cb45c4d08e)


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
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/07b1ca4c-a736-4265-9c1d-58ea86f3e15b)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/3a09f766-999a-4075-8fe9-485c0b96fcde)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/800ff245-81fd-4271-8325-bfe9a98117c0)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/df43f847-cabf-48aa-bc92-8416ce16076c)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/c7c027c9-af38-4712-aa04-dbb9dc870c09)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/d9f68051-a4f0-4127-bb81-ddade5a000bf)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/6f04d417-b882-4a22-92df-adee2fec0489)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/099c9882-2f9c-43e6-b7d6-00044298a35c)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/6daddf0c-bb8e-4109-8214-cdf5c6bbf4a0)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/d981cef0-472e-439e-9577-7062131609ec)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/17c6707b-b486-4304-bab8-388175ea40c3)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/2908b09d-d86e-4cb5-b24a-a629b773d921)


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
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/12af3f1c-f919-4cbc-949b-c8e557ff46d4)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/d9df74bc-644d-4b1c-9a47-bcb5a0b8f330)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/0c8b152f-48a5-464f-b9a5-179f80d59d28)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/46c70de8-7b64-4928-96f0-0b8a05324eee)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/3fb4f466-dc60-4a90-9b28-102cd8e05cf0)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/088a5c04-8f9e-4b03-bc81-89a4580dd429)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/02ba7daa-7898-4d8f-b78f-3faf2459eb1d)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/54f4a6a8-2f7b-4f52-827b-21378895bc96)



seq 10 
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/f1d773d3-5795-4f90-8d24-9c6616da8863)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/059de049-0a88-40c0-b4f6-c250d22597d5)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/61da2d56-9c95-40aa-a2bd-28c6d856c948)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/d7d613d4-5096-49a7-a9f7-8b1954aff317)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/b22b55b6-fa66-46c0-ab71-4b7ce943b3d0)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/33d649a0-a989-4cec-96c6-8a33b7d4cb63)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/abdd6050-e3b8-458b-a7b0-74c3b6def6a7)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/92b0420d-04c4-47dd-bec5-60dfd4583a16)


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
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/7275818e-b770-4e4c-8a11-bf0c8670af95)


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
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/2c01a6d6-496c-44d8-a2c8-670d8682492c)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/ba921dc1-ed0c-423b-a448-353f450f5a78)


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
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/440c4eae-09ea-4b7a-a478-122a8d7b365e)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/SANTHAN-2006/OS-Linux-commands-Shell-script/assets/80164014/ff4de1d2-5712-4724-842c-4dddc0735970)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Uploading image.png…]()

 
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
