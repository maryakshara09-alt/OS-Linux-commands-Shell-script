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
<img width="333" height="220" alt="Screenshot 2026-07-27 083640" src="https://github.com/user-attachments/assets/c3461a1b-73b6-40ed-b39e-c73a1a6547cf" />

cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
<img width="374" height="183" alt="Screenshot 2026-07-27 083748" src="https://github.com/user-attachments/assets/91c2736a-09b3-4d49-99a2-e16e4d1ba4fc" />

### Display the content of the files
cat < file1
## OUTPUT

<img width="485" height="168" alt="Screenshot 2026-07-27 083949" src="https://github.com/user-attachments/assets/bc3180d4-933b-4d80-b56e-4efc3e5e665a" />


cat < file2
## OUTPUT
<img width="444" height="181" alt="Screenshot 2026-07-27 084028" src="https://github.com/user-attachments/assets/c73873fe-bda1-4cd8-bfb5-b3a23012b01d" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="400" height="81" alt="Screenshot 2026-07-27 084429" src="https://github.com/user-attachments/assets/f5632ede-8839-4c6a-bcd4-be901bc040f5" />

 
comm file1 file2
 ## OUTPUT
 <img width="469" height="300" alt="Screenshot 2026-07-27 084509" src="https://github.com/user-attachments/assets/7fd53a4d-b141-46c7-86a0-61efaa779d54" />


 
diff file1 file2
## OUTPUT
<img width="432" height="289" alt="Screenshot 2026-07-27 084601" src="https://github.com/user-attachments/assets/c75d6747-808a-4e50-9a3d-44e33ddc6c42" />





### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
<img width="362" height="102" alt="Screenshot 2026-07-27 084913" src="https://github.com/user-attachments/assets/753da27f-7099-450c-b440-e9c9948fba4a" />

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
<img width="398" height="145" alt="Screenshot 2026-07-27 084953" src="https://github.com/user-attachments/assets/3a79b03e-c933-4fd8-a3fe-4a986d6b663d" />



cut -c1-3 file11
## OUTPUT
<img width="388" height="108" alt="Screenshot 2026-07-27 085053" src="https://github.com/user-attachments/assets/5323c201-20ff-4e72-a89a-08b2f4953086" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="398" height="145" alt="Screenshot 2026-07-27 084953" src="https://github.com/user-attachments/assets/6034fc84-f38d-405a-9322-447251b94693" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="361" height="119" alt="Screenshot 2026-07-27 085612" src="https://github.com/user-attachments/assets/16392538-3038-4d41-91de-70fffde31232" />


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




<img width="460" height="324" alt="Screenshot 2026-07-27 090440" src="https://github.com/user-attachments/assets/c3899a98-c922-4a43-91e0-e3b42d5b6b1e" />





grep -v hello newfile 
## OUTPUT

<img width="384" height="105" alt="Screenshot 2026-07-27 090618" src="https://github.com/user-attachments/assets/26cbb106-5d47-43bd-aef5-afa659985a2c" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="384" height="105" alt="Screenshot 2026-07-27 090618" src="https://github.com/user-attachments/assets/fb021177-635e-4cd1-9df9-a0ff1c45da5a" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="410" height="82" alt="Screenshot 2026-07-27 090703" src="https://github.com/user-attachments/assets/810b8078-5487-4310-b267-5b4eaa56d39f" />



grep -R ubuntu /etc
## OUTPUT

<img width="574" height="348" alt="Screenshot 2026-07-27 090849" src="https://github.com/user-attachments/assets/bb39e812-f247-4f39-bbf9-26f0ba581957" />



cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
<img width="382" height="195" alt="Screenshot 2026-07-27 091536" src="https://github.com/user-attachments/assets/f8de21ba-63d8-44ab-bebf-b62338c17e28" />

egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="374" height="111" alt="Screenshot 2026-07-27 091736" src="https://github.com/user-attachments/assets/7aa01dcc-c31b-4e5f-800a-5094b37c5dd6" />




egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="443" height="96" alt="Screenshot 2026-07-27 091758" src="https://github.com/user-attachments/assets/b5699f8c-2ce5-4118-9d0a-504778e1f12a" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="510" height="102" alt="Screenshot 2026-07-27 091819" src="https://github.com/user-attachments/assets/bf150071-a794-4f50-8d65-c19660c90841" />





egrep '(^hello)' newfile 
## OUTPUT

<img width="510" height="102" alt="Screenshot 2026-07-27 091819" src="https://github.com/user-attachments/assets/dac95cc2-e66f-4ae8-ae78-f188a245828c" />



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="352" height="98" alt="Screenshot 2026-07-27 091902" src="https://github.com/user-attachments/assets/b1583f0b-fe9f-4fef-a233-f717d5531e83" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="308" height="77" alt="Screenshot 2026-07-27 092435" src="https://github.com/user-attachments/assets/2194175d-c56e-4af5-8359-b1421a00809d" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="367" height="75" alt="Screenshot 2026-07-27 092457" src="https://github.com/user-attachments/assets/03d36c94-7b58-4f4b-8d6f-2c916de12b69" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="382" height="83" alt="Screenshot 2026-07-27 092517" src="https://github.com/user-attachments/assets/b289e230-9fbb-4cff-a885-d47023d69904" />


egrep l{2} newfile
## OUTPUT

<img width="382" height="83" alt="Screenshot 2026-07-27 092517" src="https://github.com/user-attachments/assets/4d46e094-191f-455d-a41d-09c1b7399b0c" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="382" height="83" alt="Screenshot 2026-07-27 092517" src="https://github.com/user-attachments/assets/bfe96cd5-d76c-4fbd-9003-b6717719e4c4" />

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
<img width="392" height="258" alt="Screenshot 2026-07-27 092908" src="https://github.com/user-attachments/assets/9b36580f-0f32-45aa-9835-53800467bce8" />


sed -n -e '3p' file23
## OUTPUT
<img width="349" height="83" alt="Screenshot 2026-07-27 092953" src="https://github.com/user-attachments/assets/2965f5c2-c6cc-4abb-b1fa-f3065e59b05c" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="401" height="249" alt="Screenshot 2026-07-27 093017" src="https://github.com/user-attachments/assets/3fabade2-e572-4fb3-ab85-7a9c18d12a5a" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="442" height="252" alt="Screenshot 2026-07-27 093042" src="https://github.com/user-attachments/assets/562df056-28c3-4a1f-9950-fadb7b1e6178" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="399" height="252" alt="Screenshot 2026-07-27 093108" src="https://github.com/user-attachments/assets/e3f253e3-2d20-4054-84cc-c171b0bb1f6f" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="390" height="178" alt="Screenshot 2026-07-27 093127" src="https://github.com/user-attachments/assets/11df6358-1a4f-4754-a474-005bd7cc10fa" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="377" height="124" alt="Screenshot 2026-07-27 093147" src="https://github.com/user-attachments/assets/141f3a7e-dff1-4d96-b7b8-d06dc3d0a3be" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="434" height="99" alt="Screenshot 2026-07-27 093226" src="https://github.com/user-attachments/assets/60a02f37-2d38-4fa1-ab07-c26c209a24ff" />


seq 10 
## OUTPUT

<img width="340" height="301" alt="Screenshot 2026-07-27 093243" src="https://github.com/user-attachments/assets/6f68788f-7221-419d-893d-1948abf69dde" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="313" height="124" alt="Screenshot 2026-07-27 093259" src="https://github.com/user-attachments/assets/244bbc8d-a580-44ca-9359-4637596c976c" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="321" height="131" alt="Screenshot 2026-07-27 093327" src="https://github.com/user-attachments/assets/2306d27b-0fc7-4e50-acec-b6af8d801008" />



seq 3 | sed '2a hello'
## OUTPUT


<img width="311" height="141" alt="Screenshot 2026-07-27 093350" src="https://github.com/user-attachments/assets/46fef52d-b681-4046-bbd5-ff8d87a445ea" />

seq 2 | sed '2i hello'
## OUTPUT



<img width="316" height="135" alt="Screenshot 2026-07-27 093407" src="https://github.com/user-attachments/assets/807405b4-78a7-4d14-b7a1-da3f74ae9c95" />




seq 10 | sed '2,9c hello'
## OUTPUT

<img width="316" height="135" alt="Screenshot 2026-07-27 093407" src="https://github.com/user-attachments/assets/22d497b9-bc76-4737-a61a-3cfaac581b87" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="402" height="127" alt="Screenshot 2026-07-27 093446" src="https://github.com/user-attachments/assets/7f49766d-69ee-4635-ac74-7cf963f43f8b" />


sed -n '2,4{s/$/*/;p}' file23

<img width="402" height="127" alt="Screenshot 2026-07-27 093446" src="https://github.com/user-attachments/assets/8f9d6d18-34a5-490f-a9cd-a1cb343b2795" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

<img width="320" height="173" alt="Screenshot 2026-07-27 094215" src="https://github.com/user-attachments/assets/63b8b086-85a7-4fd9-bb28-2ad3a4920ba4" />

sort file21
## OUTPUT


<img width="364" height="156" alt="Screenshot 2026-07-27 094244" src="https://github.com/user-attachments/assets/bcd8fa70-82f7-44fb-8579-540b9170ad83" />

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

<img width="381" height="200" alt="Screenshot 2026-07-27 094318" src="https://github.com/user-attachments/assets/e95416ad-9390-4f0b-921d-4fb0024a38ec" />


uniq file22
## OUTPUT

<img width="344" height="153" alt="Screenshot 2026-07-27 094355" src="https://github.com/user-attachments/assets/81459f1f-4f91-4037-8237-2977c23a77e1" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="424" height="251" alt="Screenshot 2026-07-27 094414" src="https://github.com/user-attachments/assets/769e4a75-39aa-40f3-86c2-a1641848ac90" />
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```

<img width="388" height="125" alt="Screenshot 2026-07-27 094457" src="https://github.com/user-attachments/assets/4ba0c123-f54b-4685-90f0-48939a3dcd41" />

cat urllist.txt | tr -d ' '
 ## OUTPUT


<img width="340" height="122" alt="Screenshot 2026-07-27 094529" src="https://github.com/user-attachments/assets/a9dc2049-c7e8-4b30-ae64-7c784d6485ab" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="461" height="81" alt="Screenshot 2026-07-27 195554" src="https://github.com/user-attachments/assets/f8203079-66fd-4a74-b593-e181d6dd31f7" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="396" height="329" alt="Screenshot 2026-07-27 195605" src="https://github.com/user-attachments/assets/f4914fe8-a384-4788-b3f7-a76088b7f6e9" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="816" height="282" alt="Screenshot 2026-07-27 195726" src="https://github.com/user-attachments/assets/8a3a5b92-f3b8-4ae5-978d-dcf0f2a03b89" />

tar -xvf backup.tar
## OUTPUT
<img width="468" height="282" alt="Screenshot 2026-07-27 195807" src="https://github.com/user-attachments/assets/12560fa7-d978-4018-9a11-e74205b33664" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="587" height="133" alt="Screenshot 2026-07-27 195901" src="https://github.com/user-attachments/assets/28c098a1-cf21-43d1-adfa-3b112fc41254" />
 
gunzip backup.tar.gz
## OUTPUT

 <img width="412" height="61" alt="Screenshot 2026-07-27 195939" src="https://github.com/user-attachments/assets/d1aaed0a-ea15-4953-9ee1-48201ed6726b" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="510" height="107" alt="Screenshot 2026-07-27 200300" src="https://github.com/user-attachments/assets/3d3f902d-70df-49bd-bc49-7eb0006be8ee" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```
<img width="520" height="158" alt="Screenshot 2026-07-27 200349" src="https://github.com/user-attachments/assets/f908a2f3-9274-4100-b848-dd5f4812001d" />


cat herecheck.txt
## OUTPUT

<img width="448" height="348" alt="Screenshot 2026-07-27 200438" src="https://github.com/user-attachments/assets/d45baf34-91cb-4b40-adc0-1ebf1f3b1e98" />

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

<img width="455" height="331" alt="Screenshot 2026-07-27 200516" src="https://github.com/user-attachments/assets/1ecf49a1-7a6a-456d-af6e-711675ff336d" />
<img width="630" height="457" alt="Screenshot 2026-07-27 200612" src="https://github.com/user-attachments/assets/dfb77c8c-704d-4e26-9445-c660dacca828" />
 
ls file1
## OUTPUT
<img width="622" height="88" alt="Screenshot 2026-07-27 200655" src="https://github.com/user-attachments/assets/af54d7f3-0b07-4042-b316-0d7e324ba6cf" />

echo $?
<img width="405" height="77" alt="Screenshot 2026-07-27 200705" src="https://github.com/user-attachments/assets/7d5df6ad-688a-4e32-a495-326310b74bb4" />

## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="513" height="155" alt="Screenshot 2026-07-27 200752" src="https://github.com/user-attachments/assets/4c181328-b7f4-4e88-9a42-e5376c6dd4cb" />
 
abcd
 
echo $?
 ## OUTPUT

<img width="401" height="150" alt="Screenshot 2026-07-27 200833" src="https://github.com/user-attachments/assets/fd5afff6-124a-49fe-be14-be9167d39f3a" />

 
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

<img width="424" height="297" alt="Screenshot 2026-07-27 201305" src="https://github.com/user-attachments/assets/a0b57ec3-adaa-4e8b-82e8-5dfaa6911887" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="696" height="155" alt="Screenshot 2026-07-27 201340" src="https://github.com/user-attachments/assets/b01130b0-684f-43bc-b8ef-07f484ebc4ec" />


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
<img width="710" height="259" alt="Screenshot 2026-07-27 201417" src="https://github.com/user-attachments/assets/dd0f0aac-286c-4a29-8f1b-c6e6c5d5b6c2" />

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

<img width="530" height="347" alt="Screenshot 2026-07-27 201515" src="https://github.com/user-attachments/assets/b6d93084-b4b1-4395-9d2f-73cc42667726" />


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
<img width="530" height="347" alt="Screenshot 2026-07-27 201515" src="https://github.com/user-attachments/assets/6ea432c1-0a91-41f3-8d83-ca676692432c" />

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
<img width="530" height="347" alt="Screenshot 2026-07-27 201515" src="https://github.com/user-attachments/assets/0bb78e32-9a59-4c57-9d14-960afc85c22f" />

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
