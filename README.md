# linux-cheat-sheet
List of most basic Linux commands

ssh
=
Connect to a remote host machine

```
ssh username@hostname
```
 
ls
=
List all the files in the current working directory

```
# list all the files
ls -l 

# list all the files including hidden ones
ls -la
```

pwd
=
Print working directory

```
pwd
```

cd
=
Change directory

```
cd path/to/directory
```

touch
=
Create a file

```
touch <file_name>
```

echo
=
Add content to a file or just print stuff

```
echo "Hello World"
echo "Hello World" > helloworld.txt
```

nano
=
Edit file

```
nano <file_name>
```

vim
=
Edit file

```
vim <file_name>
```

cat
=
Print the content of a file

```
cat <file_name>
```

shred
=
Giberish the content of a file

```
shred <file_name>
```

mkdir
=
Create a new directory

```
mkdir <name_of_directory>
```

cp
=
Copy file

```
cp <file_to_copy> <path/to/target/directory>
```

mv
=
Move file

```
cp <file_to_move> <path/to/target/directory>
```

rm
=
Remove file

```
rm <file_name>
```

rmdir
=
Remove empty directory

```
rmdir <directory_name>
```

rm -r
=
Remove directory recursively


```
rm -r <directory_name>
```
 
ln
=
Link to a file

```
# -s  soft
ln -s <file_name> <link_to_file>

# e.g.
ln -s test.txt linkToFile
```

clear
=
Clear the terminal

```
clear
```

whoami
=
Current user

```
whoami
```

useradd
=
Add a new user

```
useradd <name>
```

sudo
=
Root user permissions

```
sudo useradd <name>
```

adduser
=
Add user with additional parameters

```
sudo adduser <name>
```

su
=
Switch user

```
su <user_name>
```

exit
=
Exit current service/session

```
exit
```

passwd
=
Add password to user

```
sudo passwd <user_name>

# change root user password
passwd
```

apt
=
Package manager

```
sudo apt update
sudo apt install <package_name>
```

finger
=
Inspect another user

```
finger <user_name>
```

man
=
List command help

```
man <command>

# e.g.
man ls
```

whatis
=
Show info about command

```
whatis <command>
```

which
=
Path to command

```
which <command>
```

whereis
=
All paths to command

```
whereis <command>
```

wget
=
Get stuff from internet

```
wget <download_link>
```

curl
=
Get stuff from internet

```
curl <download_link>

# or download and put into another file

curl <download_link> > file.txt
```

zip
=
Compress

```
zip <name> <file_to_zip>
```

unzip
=
Decompress

```
unzip <file>
```

less
=
Display one page at a time

```
less <file>
```

head
=
Display beginning of a file

```
head <file>
```

tail
=
Display end of a file

```
tail <file>
```

cmp
=
Compare two files

```
cmp <file_1> <file_2>
```

diff
=
Display differences between two files

```
diff <file_1> <file_2>
```

sort
=
Sort content alphabetically

```
cat <file> sort
```

find
=
Find files using regex

```
sudo find <directory> -name "<regex>"

# find all hidden files
find . -type f -name ".*"

# find all empty directories
find . -type f -empty

# find all executable files
find . -perm /ax
```

chmod
=
Change file attributes

```
# make file executable
chmod +x <file_name>
```

chown
=
Change ownership of file

```
chown <user_name> <file_name>
```

ifconfig
=
IP address

```
ifconfig
```

ip address
=
IP address

grep
=
Grep stuff

```
ip address grep eth0 grep inet
```

awk
=
Awk stuff

```
ip address grep eth0 grep inet awk '{print $2}'
```

resolvectl status
=
DNS info

```
resolvectl status
```

ping
=
Check website status

```
ping google.com

# trace route to website
traceroute google.com
```

netstat
=
Display ports info on local machine

```
netstat -tulpn
```

ss
=
Same as netstat

```
ss -tulpn
```

iptables
=
Forward ports

```
# forward port 80
sudo iptables -I input -p tcp -m tcp --dport 80 -j ACCEPT
```

ufw
=
Forward ports

```
sudo ufw allow 80

# see what is allowed
sudo ufw status

# enable ufw
sudo ufw enable
```

uname
=
Info about system

```
uname

uname -a
```

neofetch
=
Display system info

```
sudo apt install neofetch

neofetch
```

cal
=
Calendar

```
cal
```

free
=
Check how much memory you have available

```
free
```

df
=
Check how much space you have available

```
df -H
```

ps
=
List of processes running on your sistem

```
ps

ps -aux
```

top
=
List of most memory consuming processes

```
top
```

htop
=
Same as above but prettier

```
htop
```

kill
=
Kill a process

```
ps -aux grep <process_name>

kill -9 <process_id>
```

pkill
=
Kill a process without knowing the process ID

```
pkill -f <process_name>
```

systemctl
=
Start stop or restart services or daemons

```
systemctl stop <service>

systemctl start <service>

systemctl restart <service>

systemctl status <service>
```

history
=
History of all used commands

```
history
```

reboot
=
Restart system

```
sudo reboot
```

shutdown
=
Shutdown system

```
# shutdown in ~ 1 min
sudo shutdown

# shutdown now
sudo shutdown -h now
```
