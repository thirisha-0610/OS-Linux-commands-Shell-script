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
![304675248-87ac0d6a-1446-457d-86a1-988721ea01af](https://github.com/user-attachments/assets/a57bbcc5-53a5-42ab-a95a-b1573d3a592a)

cat < file2
## OUTPUT
![304675707-8fccc8a1-d8c7-490c-954c-8d12780ad55d](https://github.com/user-attachments/assets/02b69943-eeab-4674-9521-3f6943ccaa51)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![304675947-faf7be7f-368e-4972-a142-bdb707f5ef60](https://github.com/user-attachments/assets/ccd7b31e-2a62-4603-8685-912f40627687)

comm file1 file2
 ## OUTPUT

 ![304676166-a7a105ea-6765-4fd6-b997-014bbd767c2a](https://github.com/user-attachments/assets/7d6c587d-a051-4734-b311-b3a07a4e87dc)

diff file1 file2

## OUTPUT

![304676399-01ad1a86-1512-4ffd-9dd0-33ad1b981581](https://github.com/user-attachments/assets/63107886-c989-42ee-9119-a7b18dc75e65)

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
![304677935-a0cce53d-e73e-455e-9340-72b81f67ad6d](https://github.com/user-attachments/assets/2e7e71b1-91c6-44bf-8718-4e767322356f)

cut -d "|" -f 1 file22
## OUTPUT

![304679935-e7a008d1-3e4c-40d2-a3a5-44ba333b2e4f](https://github.com/user-attachments/assets/edc0e1f0-fca0-4e4a-ae52-8bb370c8131d)

cut -d "|" -f 2 file22
## OUTPUT
![304680064-c5735266-0638-486c-a756-e6b0340deb48](https://github.com/user-attachments/assets/4990326f-1a51-45a3-bca5-f50e77ecb5ea)

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

![304678745-b702dd82-0b07-4005-b957-0cc15c1d3d23](https://github.com/user-attachments/assets/33015d7a-bd9a-4400-9a39-edce4b2582ff)

grep hello newfile 
## OUTPUT

![304678833-08ea546b-76f1-4eda-9e0f-f203f280e2a6](https://github.com/user-attachments/assets/082911e4-5f8e-423a-9877-412307ceb1c4)

grep -v hello newfile 
## OUTPUT

![304679348-45040c17-58c3-446f-aa3f-077eb70a68f3](https://github.com/user-attachments/assets/cb8eefc3-5d28-4657-93d8-a83a472a7d65)

cat newfile | grep -i "hello"
## OUTPUT

![304679551-d193581f-02b6-4555-b088-7b05d7461148](https://github.com/user-attachments/assets/5147f8c9-347b-46d9-a4f2-a47911ca90fa)

cat newfile | grep -i -c "hello"
## OUTPUT

![304680860-65a8474e-cc02-4c2d-9e67-8e76ee6c4584](https://github.com/user-attachments/assets/94f49554-1ad1-4420-bfab-2c58cec56818)

grep -R ubuntu /etc
## OUTPUT

![309630290-22fdcf81-932f-4b8d-8525-a64e0ec2f425](https://github.com/user-attachments/assets/fe63d40e-6773-412d-acb4-6d0120468dc0)

grep -w -n world newfile   
## OUTPUT
![305804614-3e1bda9a-6ea0-4db2-a568-fbc718c37a19](https://github.com/user-attachments/assets/1c7c6bda-6636-43c5-95d8-b8f828628482)

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

![305808474-25d0fec3-0f33-4029-bb7a-8b6dc3d9f165](https://github.com/user-attachments/assets/a9e483ec-0c41-405e-bb29-3fed12c4cac0)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![305809631-949add15-11a4-4fe7-84e8-440126aaa9a4](https://github.com/user-attachments/assets/9a616b71-ac26-4cbf-bcd6-0b4319cfab7a)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![305810476-30add5da-a3a2-4363-a53a-130b58db8320](https://github.com/user-attachments/assets/daeaeed8-42e7-464f-8f8d-ff5ca98040ef)



egrep '(^hello)' newfile 
## OUTPUT
![305811443-55b62521-ae26-4c21-a7ef-76af4069aca8](https://github.com/user-attachments/assets/3dc810c7-e48f-4660-936b-5b91050644b5)



egrep '(world$)' newfile 
## OUTPUT
![305812168-6231c0d4-c8b0-4331-80ab-b50c2c750dfa](https://github.com/user-attachments/assets/ff733263-c707-4aa3-9f32-b6d0fc611ed3)



egrep '(World$)' newfile 
## OUTPUT
![309630312-54bd99ae-8395-4423-a4d5-33985e59bf47](https://github.com/user-attachments/assets/b3285124-3e11-4af7-a98e-0bd6b5126165)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![305814671-f34d417b-508e-4569-8d0e-e8a3ad4d6b45](https://github.com/user-attachments/assets/9e85dc5b-f974-4938-bab1-395680090d98)



egrep '[1-9]' newfile 
## OUTPUT
![306316795-d39364c0-71da-42bc-844d-be536727a70f](https://github.com/user-attachments/assets/e6dcbee0-c809-4028-a6c5-76ba596cd93d)



egrep 'Linux.*world' newfile 
## OUTPUT

![306317421-7149b0f0-5880-435e-8c34-0114f0fa3f94](https://github.com/user-attachments/assets/06261923-c788-411c-a36e-39e42f34e336)

egrep 'Linux.*World' newfile 
## OUTPUT

![309630686-a1558cfd-123d-4d04-a072-edf7f8e194de](https://github.com/user-attachments/assets/c842bb59-b1ba-41f5-9fd5-72ba27a5aa83)

egrep l{2} newfile
## OUTPUT

![306318648-919d40e4-c1ea-42e1-9645-de17925281f8](https://github.com/user-attachments/assets/08642e5e-08be-4ec7-bcba-20aef8d8b68f)


egrep 's{1,2}' newfile
## OUTPUT 

![306319020-cea59baf-267b-419f-aee4-2673da56d2d5](https://github.com/user-attachments/assets/95c6e208-d704-47cb-b692-fd264bf95e8d)

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

![306320295-98b8fafa-04d2-41ed-ad0a-f1230817d95a](https://github.com/user-attachments/assets/bc13707f-b20e-49a0-854b-c33ebb122b86)


sed -n -e '$p' file23
## OUTPUT
![306320509-b660c572-1734-40ce-be88-9252a60d9aa3](https://github.com/user-attachments/assets/794fcb6c-d6c6-48be-b4e9-4affa4f45e47)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![306320967-dbb7abdd-1f69-4e0f-8433-2953261eb789](https://github.com/user-attachments/assets/e96317a6-b36e-4282-9c6f-b83916b53cba)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![306322946-6aa29cfd-6b07-4d27-b36e-1b14d1cb2e7e](https://github.com/user-attachments/assets/cdf4d9b1-afb6-4550-ab38-8cac3fb01b36)


sed  '/tom/s/5000/6000/' file23
## OUTPUT


![309630812-30f5c5a9-9c75-43f0-8ad1-38df5d8c8177](https://github.com/user-attachments/assets/96ac7379-326e-4c25-90d4-0eb59d108d64)

sed -n -e '1,5p' file23
## OUTPUT

![306323531-0257c450-9623-4f9c-a9fa-376e59ea41eb](https://github.com/user-attachments/assets/afdaceb4-87a5-4933-9d94-058353dbeef9)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![306324580-13bd70de-b1df-4d66-91f4-400ca29f4092](https://github.com/user-attachments/assets/607070e1-3801-4b6f-bdb3-ad6d81cad476)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![306324859-f4130ac3-9533-4d96-8f07-cabd48ddeb4b](https://github.com/user-attachments/assets/c9af429f-1574-4c0c-9a9e-b7358fa70639)


seq 10 
## OUTPUT

![306325086-6878d8f6-6916-4079-9662-041241ba0fb7](https://github.com/user-attachments/assets/0e0fb4c3-6479-4e3d-b480-e6c83690a6eb)


seq 10 | sed -n '4,6p'
## OUTPUT

![306325371-81bde4e8-4de7-46ae-a6ab-91a67224ad05](https://github.com/user-attachments/assets/fc325015-cfe6-4c7e-818e-f189f8cd56fa)


seq 10 | sed -n '2,~4p'
## OUTPUT

![306325717-fd8471e6-bc9a-43b1-aa5d-573add27fa89](https://github.com/user-attachments/assets/fd7c6cf4-bf93-42ff-aa1f-576494b3ea53)

seq 3 | sed '2a hello'
## OUTPUT
![306327286-444759b0-3989-40f1-add9-59938cbb27f1](https://github.com/user-attachments/assets/fbeb2d4d-47e5-4712-a516-7e866e1814ec)

seq 2 | sed '2i hello'
## OUTPUT
![306327545-f725afb5-e8b8-4694-b49c-b8a0c813a692](https://github.com/user-attachments/assets/80b2dcb1-bd3a-42d5-b9a9-b5df5c3a117a)


seq 10 | sed '2,9c hello'
## OUTPUT

![306327729-a00f2a8c-4b7d-4822-99cf-83263a691c6a](https://github.com/user-attachments/assets/ff05324d-4713-430d-ba45-946964447179)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![306328394-d04ee7c2-46ee-43ac-93b2-0ea156edc231](https://github.com/user-attachments/assets/76cfefb1-bf43-44e8-a750-485dcd825d4d)


sed -n '2,4{s/$/*/;p}' file23
### OUTPUT

![306328394-d04ee7c2-46ee-43ac-93b2-0ea156edc231](https://github.com/user-attachments/assets/d8b8550f-e827-4e2e-bd12-8ee4b35be4de)


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
![306330202-0fa515bd-81b8-4cb3-8d49-4e050065141e](https://github.com/user-attachments/assets/eac2e945-6653-4422-8582-87228bd34483)


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

![306330904-47a9031a-70e8-4290-ab78-aee3b3336700](https://github.com/user-attachments/assets/8641b525-8737-440f-9b7d-7d27c42e7603)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![306331301-3a8b94a3-b62c-4e2d-ba61-6b952493ee12](https://github.com/user-attachments/assets/40153662-b888-4ce2-a62d-f9d19b0dae28)

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
![306538649-bfeb1938-f6da-4d70-a305-87724b6f9b66](https://github.com/user-attachments/assets/ef013a03-8cc5-4cd5-aa78-aac36db878f3)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![306538982-a0a2671d-6f19-4682-bd0d-36e82d2a7048](https://github.com/user-attachments/assets/f5a138e7-9913-4f26-af94-9b62fe69b708)


#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![309631309-4c9a04e6-dfe5-4928-af8f-b4f35f38d37c](https://github.com/user-attachments/assets/6a798d35-dbbf-43ab-8e47-717a5cc1783e)

tar -xvf backup.tar
## OUTPUT
![309631412-ccbc4154-17d8-4dc5-bbaf-0896a668b8a5](https://github.com/user-attachments/assets/c3f2985b-a499-47d4-aa92-9af2848d924f)
```
tar -xvf backup.tar
```
### OUTPUT

![309631509-0d5efaa0-863c-4b17-9ed8-3e9dd6f09955](https://github.com/user-attachments/assets/154cfaae-e69f-4f20-b85c-e807e36e1868)

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
![309631646-8b571dc0-2f93-4ab2-a314-0055d7559ee3](https://github.com/user-attachments/assets/36eb897f-db6e-4896-adf4-d4fe5ce96429)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![306541597-f05197ce-9a61-4432-8677-06f9a3f2074d](https://github.com/user-attachments/assets/ec03ed36-ba6d-4eff-af34-3c104a978bae)


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
![309631701-66ce463b-a769-4ce7-9701-472a735ec84e](https://github.com/user-attachments/assets/fa266f9d-a128-4197-9317-62fe0cb653e4)

 
ls file1
## OUTPUT
![306542056-6d43e64c-5b38-4b4c-953d-15306e4f0962](https://github.com/user-attachments/assets/1a1c8f31-0522-40e0-9fd8-8727ba3012e1)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![306542294-e207d92e-1b49-4f24-bf5e-6b509e151ca3](https://github.com/user-attachments/assets/f2e61dc6-24fc-4e48-a9da-0e4aabc0087f)

abcd
 
echo $?
 ## OUTPUT

![309631818-84516bf6-930b-4545-8031-e8922ded7758](https://github.com/user-attachments/assets/14942117-1054-4436-8c30-6c505da1a7a0)

 
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

![307678773-f5691f96-7fb8-405b-aca8-99b245694866](https://github.com/user-attachments/assets/b0aaa81a-ebbf-4989-a91c-949f0b9534ed)

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
![307679532-9e14508f-e06b-48bd-8335-24ab45869507](https://github.com/user-attachments/assets/f0ac1f47-6542-4c7d-83a2-d8c467214dde)

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

![307680054-a3bbfe31-a584-41fa-bb8e-34f6a8c71c2d](https://github.com/user-attachments/assets/c1f68c70-eafa-4a88-93f3-86b459568244)


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

![307680530-f0324dc3-e174-4c13-9e62-2b8e12f0ece8](https://github.com/user-attachments/assets/661713cf-bdb2-47e7-93cf-28ed5ce978b1)

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
![307681129-4d51cbe0-75a7-4c8b-9897-31d80e242b23](https://github.com/user-attachments/assets/e48c55c5-5fef-4e18-9e86-4223a0b44ce0)


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

![307682021-b23da05d-9057-4155-a3b3-e0d5e1658424](https://github.com/user-attachments/assets/c1bc5615-f861-4a04-b908-60235a747e18)

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
![307682427-dd2856b3-6746-4001-9bb5-64248d70cbf2](https://github.com/user-attachments/assets/c29f8ed3-c118-4b2b-bb50-a225b5b484cd)

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
### OUTPUT
![307682893-2089b93c-f8f4-4aa2-9a14-7ad18c022649](https://github.com/user-attachments/assets/96112688-b88e-459a-bab6-ce5278339ea3)

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
### OUTPUT

 ![309632182-01d121de-472d-4dbd-b7b9-3b02b5273151](https://github.com/user-attachments/assets/4ecfed5c-e79e-409c-95e4-16d0d7de830a)

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
 
### OUTPUT
![309632243-37852111-38c2-4d5b-b02e-db081bb55911](https://github.com/user-attachments/assets/6033c2d8-dab8-4512-99cb-83f736af747a)

 
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
 ![308472685-5db0aa23-2b65-47be-845b-d27e71d1cf0e](https://github.com/user-attachments/assets/e96cac5b-2d74-4c9a-a2ca-7844f3ba75e7)

 
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
### OUTPUT

 ![308473693-e871a57b-eba5-4f24-beaa-b50a1cc05f9d](https://github.com/user-attachments/assets/945b036e-e5a5-4aa2-8029-244297a98c3d)

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
### OUTPUT 

 ![308474292-3e502c00-aa25-42d7-94f4-c1cf42abbeb0](https://github.com/user-attachments/assets/193873b1-71b5-40cb-bc0c-02f5a65ff5ef)

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

![308474845-57eb9b7e-55ed-4f8a-b04f-299ca7312d54](https://github.com/user-attachments/assets/1305c3c5-e96f-427a-8eb1-75a6267bb28b)

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
### OUTPUT
![309632485-a2fc3dd0-6460-481c-93c6-644032cf66bf](https://github.com/user-attachments/assets/cb9dfa4f-5896-4ceb-911f-f5649f400ac4)



$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![367221845-a5b30984-08a4-44e8-9208-20105171a0c3](https://github.com/user-attachments/assets/041142f6-65ee-46b2-a0cc-aaa2a735aa54)



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
![367221845-a5b30984-08a4-44e8-9208-20105171a0c3](https://github.com/user-attachments/assets/b705e55e-51ee-4400-9a02-2990bd78fd3a)

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
![367222602-28a50bca-a0f9-48b4-8e32-736a52421e50](https://github.com/user-attachments/assets/3a4510cc-92ef-455e-947c-57b60b3e1923)

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

 ![367222671-f0959f28-d0ea-4596-af33-ce9ee42c98bd](https://github.com/user-attachments/assets/dd32ae9d-03f7-45b5-a13e-337f807f5ea9)

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
![367222816-2b9ff9eb-c421-43f7-be17-80534ae70235](https://github.com/user-attachments/assets/e9720aca-556d-4af1-bfc4-63f5189e2965)

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
 ![367222979-7e0a5401-2cf3-4890-9a6b-28f68bab86d4](https://github.com/user-attachments/assets/0ac87190-a1bf-4034-a266-d151c166db2c)

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
![367223539-bc316ef4-2b6c-4eac-8cb4-62f1cd22b96e](https://github.com/user-attachments/assets/18af2b0e-4cfc-4aaf-bb97-126c789628e8)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![367223623-0058d1db-7642-4214-b403-2feda95c8ec3](https://github.com/user-attachments/assets/4652bcf4-de5e-46f6-8f53-988fece8117e)


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
![367223782-a64e3dea-a0b2-4ef6-87dc-ce5586af343d](https://github.com/user-attachments/assets/27f8f964-0f4b-471f-bbe2-a5df7e74277f)

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
 ![367223998-ed654d0b-6131-4054-9315-07658e9fbd95](https://github.com/user-attachments/assets/b9f522ff-18dc-4915-b784-88c593bf116f)

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
 ![367224148-496372ba-f016-4811-b096-d4c8346fe431](https://github.com/user-attachments/assets/56f185d3-c4c9-45ed-a12d-23e53efc91a7)

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
 ![367224273-5a87aa69-a179-43b9-bcd7-ef646c9cefef](https://github.com/user-attachments/assets/b140fe9a-9a9f-4ae9-b6fc-60c4f09514bc)

 
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
 ![367224497-5a974231-3dca-4896-a728-9f7c2df00e26](https://github.com/user-attachments/assets/69bed850-7e60-459b-911d-3089821e7a20)

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
![367224574-715391d3-abad-4f7b-905f-e2b063b2bca0](https://github.com/user-attachments/assets/dfe2b770-6374-4445-a87b-70551156f294)


# RESULT:
The Commands are executed successfully.
