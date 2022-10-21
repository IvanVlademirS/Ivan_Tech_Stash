# Getting Started

*NOTE: Using Linux MINT*

### CLI Intro
- CASE SENSITIVE! 
- (user) @ (host)
- after colon, current working directory is shown
- $ = normal user, admin = # sign
- ls - list
- whoami - current user
- hostname - current host
- pwd - current directory
```bash
whoami
Whoami
hostname
pwd
ls
cd files
cd ..
```

### Help in the CLI
- use manual (man) and help (--help), or info command for more document look
- can use https://explainshell.com/# visual help on commands
```bash
man ls
info ls
ls --help
```

### CLI Arguments & Options
- can combine more than one option that uses single character, but can't combine multi-character formats
```bash
man ls
ls -al
ls --all -l
man ls
ls
ls -I "file*"
ls --ignore="file*"
```

### Looking at Text Files
- use more or less
```bash
ls
more wordlist.txt
less wordlist.txt
more image.jpg
```
- cat command - concatonate 
```bash
man cat
ls
cat file1.txt
cat file3.txt
cat file1.txt file3.txt
cat file3.txt file1.txt
cat
Hello world
man cat
cat -b file3.txt file1.txt
cat -n file3.txt file1.txt
cat file3.txt file1.txt > combined.txt
cat combined.txt
cat > new-file.txt
Hello world
Ctrl+D
cat new-file.txt
```

# Files and Filesystem

### Linux Filesystem Hierarchy Standard
- can view details with man command
```bash
man hier
```

### Devices, Partitions, Mounting
- commmands
	- df - disk file system space usage of all mounted systems
	- du - disk usage
```bash
mount
df -h
du -sh ~
```

### Absolute and Relative Paths
- An absolute path is defined as specifying the location of a file or directory from the root directory(/)
	- valid from anywhere on filesystem
	- usually longer
- Relative path is defined as the path related to the present working directly(pwd)
	- generally shorter and easier to use
```bash
ls /home/bob/files/notes.txt
cd /var/log
ls /home/bob/files/notes.txt
ls /home/bob/files/no-such-file.txt
cd /home/bob
ls files/notes.txt
ls ./files/notes.txt
cd files
ls notes.txt
ls ./notes.txt
cd ../backup
ls ../files/notes.txt
cd /var/log
ls ../../home/bob/files/notes.txt
```

### Working with Files & Directories
- touch - make empty file
- cp - copy
- mv - move
- rm - remove
- mkdir - make directory
- rmdir - delete directory
```bash
ls -l notes.txt
touch notes.txt
ls -l notes.txt
touch test.txt
ls test.txt
cp notes.txt notes-copy.txt
man cp
mv notes-copy.txt ../backup/
ls ../backup
rm ../backup/notes-copy.txt
ls ../backup
man rm
mkdir project
cd project
cd ..
rmdir project
ls non-empty-dir/
rmdir non-empty-dir
rm -rf non-empty-dir
mkdir project
mv project project01
```

### Spaces in Paths & Filenames
- bash shell uses spaces as separator for CLI arguments
- can use \ or quotes to specify literal value
- best practice is to not use spaces in files or directory names
```bash
cd spaces
ls
cat file name.txt
cd my dir
cat file\ name.txt
cd my\ dir
cd ..
cat "file name.txt"
```

### File and Path Expansion
- can expand with wildcard
	- if not working, need to set the globstar option
- commonly called globbing
```bash
ls file*.txt
ls file?.txt
ls **/*.txt
shopt -s globstar
ls file[123].txt
ls file[1-3].txt
ls file[a-zA-Z].txt
```

### Looking at Text Files 2
- head - first 10 lines, -n option for different number
- tail - last 10 lines, options are similar to head
	- can use to monitor file for changes, e.g. logs
- diff - can show differences between files in CLI
```bash
head wordlist.txt
head -n 5 wordlist.txt
head -5 wordlist.txt
tail wordlist
tail -n 5 wordlist.txt
tail -5 wordlist.txt
tail -f /var/log/auth.log
<in another terminal> sudo ls
diff file1.txt file3.txt
```

### Hard and Soft Filesystem Links
- Links - reference or pointer to file or directory in the filesystem
- Hard - points to physical location in storage, usually for files
- Soft - usually used to point to directories, can cross filesystems
```bash
Hard and Soft Filesystem Links
cat hello.txt
ln hello.txt hello-hard-link.txt
<edit hello.txt>
cat hello.txt
cat hello-hard-link.txt
ls -l hello*.txt
rm hello.txt
cat hello-hard-link.txt
ln hello-hard-link.txt hello.txt
ln -s ./hello.txt hello-soft-link.txt
ls -l hello*.txt
```

### Compressing & Archiving Files
- can use zip, unzip
- tar - to compress file(s)
- gunzip - to decompress file(s)
```bash
man zip
zip tmp/backup-files.zip file1.txt file2.txt file3.txt
ls tmp
unzip -l tmp/backup-files.zip
ls dir1 dir2
zip tmp/backup-dirs.zip dir1 dir2
unzip -l tmp/backup-dirs.zip
rm tmp/backup-dirs.zip
zip -r tmp/backup-dirs.zip dir1 dir2
unzip -l tmp/backup-dirs.zip
man tar
tar cvf backup.tar file?.txt dir? shakespeare.txt
tar tvf backup.tar
cd test
tar xvf ../backup.tar
ls
ls dir?
rm -rf *
cd ..
ls -lh backup.tar
gzip backup.tar
ls -lh backup.tar.gz
gunzip backup.tar.gz
ls
tar cvfz backup2.tar.gz file?.txt dir?
ls -l backup2.tar.gz
```

### Searching the Filesystem
- find - search for files in a directory hierarchy
- locate - quickly finding files and directories, uses database
- which - use to find where commands are
```bash
man find
find . -name 'file*.txt'
find . -iname 'file*.txt'
locate file.txt
locate file*.txt
locate -i file*.txt
which ls
```

# Users and Groups

### Working with Users and Groups
- users - only prints user
- who - most commonly used
- w - provides most info
```bash
users
who
w
less /etc/passwd
less /etc/group
ls -la /home
```

### File and Directory Permissions
- read, write, execute (rwx)
- (user)(group)(all)
- use chmod to change permissions, symbolic and octal mode (4, 2, 1)
- use chown to change file owner or group
- use chgrp to change group ownership
```bash
ls -l
man chmod
ls -l hello.txt
chmod g-w hello.txt
ls -l hello.txt
chmod a=,u=r hello.txt
ls -l hello.txt
chmod 664 hello.txt
ls -l hello.txt
man chown
ls -l hello.txt
chown sally hello.txt
ls -l hello.txt
chgrp sally hello.txt
ls -l hello.txt
```

### Changing Users
- sudo - super user do, used to execute as root
- su - switch user
```bash
cat /etc/shadow
sudo cat /etc/shadow
cat /home/sally/sample.txt
ll /home/sally/sample.txt
sudo -u sally cat /home/sally/sample.txt
su sally
```

### Changing Passwords
- passwd command
```bash
man passwd
passwd
<enter wrong password>
passwd
sudo passwd sally
```

# Installing Software

### Package Management
- packages = apps
- package mgmt systems handle dependencies for user(s)

### Debian Systems
- use deb packages
- 2 main program: dpkg (d-package) and apt (most commonly used)
```bash
man dpkg
apt update
apt list --upgradable
apt upgrade
which pdftk
apt search pdftk
apt show pdftk
apt install pdftk-java
which pdftk
apt remove pdftk-java
apt purge pdftk-java
apt autoremove
```

### RedHat Systems
- use rpm packages
- yum - similar to apt
```bash
sudo yum check-update
sudo yum update
yum search qpdf
yum info qpdf
sudo yum install qpdf
which qpdf
yum remove qpdf
```

### Manually Installing Software
- use wget to download
- use tar to extract
- example installing git:
```bash
apt install build-essential automake checkinstall libz-dev libssl-dev libcurl4-gnutls-dev libexpat1-dev gettext cmake gcc curl
which git
cd Downloads
wget https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.29.3.tar.gz
tar xfz git-2.29.3.tar.gz
ls
cd git-2.29.3/
less INSTALL
./configure
make
sudo make install
git --version
```

# Shells

### Environment Variables
- stores config info
```bash
printenv | less -S
COUNT_LOCAL=42
echo $COUNT_LOCAL
42
echo COUNT_LOCAL
COUNT_LOCAL
echo $COUNT_LOCAL
exit
export COUNT_GLOBAL=55
echo $COUNT_GLOBAL
55
echo $COUNT_GLOBAL
55
unset COUNT_GLOBAL
echo $COUNT_GLOBAL
```

### Startup Files
- interactive non-log in shell = what we are using
- alias = keyboard shortcut
```bash
ls -al ~
nano .bashrc
<Add lines>
alias del='rm -rfi'
alias c='clear'
<Save and exit>
c
<new shell>
ls
c
<original shell>
source .bashrc
c
```

### Redirecting Input and Output
- std in, out, err
- use >> to append to a file
- use &> or 2> to redirect stderr
```bash
sudo ls /root
ls /root
ls /etc/
ls /etc/ > ~/dir-contents.txt
less ~/dir-contents.txt
ls /tmp/
ls /tmp/ > ~/dir-contents.txt
less ~/dir-contents.txt
ls /etc/ >> ~/dir-contents.txt
less ~/dir-contents.txt
clear
head /etc/passwd
head < /etc/passwd
clear
find / -name 'sample.txt'
find / -name 'sample.txt' 2> errors.txt
less errors.txt
find / -name 'sample.txt' 2> /dev/null
cat /dev/null
find / -name 'sample.txt' &> all.txt
less all.txt
find / -name 'sample.txt' > all.txt 2>&1
find / -name 'sample.txt' > location.txt 2> /dev/null
cat location.txt
```

### Pipes
- connect std out to std in 
- use | 
```bash
ls -l /etc/ | less
ls -l /etc/ | head -n 20 | tail -n 5
find / -name 'sample.txt' | less
find / -name 'sample.txt' |& less
```

### Command History
- history - see all previous commands
- use ! with history # to execute command in history
```bash
history
history | tail
!<insert command #>
!10
!-1
!!
!cat
cat file1.txt
^file1.txt^fileA.txt^
history
less ~/.bashrc
```

### Command Substitution
- replace command with its output before command is executed
```bash
cat file-list.txt
cat file-list.txt | ls -l
ls -l < file-list.txt
ls -l `cat file-list.txt`
ls -l cat file-list.txt
ls -l $(cat file-list.txt)
```

# Utilities

### Search and Process Text
- grep - searches for patterns, becomes powerful when searching multiple files
- sort - sort file content
- uniq - filter adjacent duplicate lines , can sort first so lines are adjacent then use uniq to filter our duplicates
- wc - word count, prints lines, words, and bytes of file
```bash
man grep
grep bob wordlist.txt
grep -v e wordlist.txt | less
grep error /var/log/*.log
grep error -A 1 -B 3 /var/log/*.log
cat random-words.txt
sort random-words.txt
cat random-numbers.txt
sort -nr random-numbers.txt
man uniq
less random-words.txt
uniq random-words.txt
sort duplicates.txt | uniq
wc wordlist.txt
grep bob wordlist.txt | wc -l
clear
grep -v e random-words.txt
grep -v e random-words.txt | sort
grep -v e random-words.txt | sort | uniq
grep -v e random-words.txt | sort | uniq | wc -l
```

### Manipulating Text
- sed - stream editor for filtering and transforming text
- awk - similar to sed, but breaks each line of input into separate field or columns 
```bash
man sed
cat sample.txt
sed 's/Suite/Ste/' sample.txt
echo Suite Suite | sed 's/Suite/Ste/'
echo Suite Suite | sed 's/Suite/Ste/g'
sed '$s/Suite/Ste/g' sample.txt
sed '/Suite/d' sample.txt
grep Suite sample.txt
sed '/ee/ s/Suite/Ste/g' sample.txt
sed 's/$/\n/g' sample.txt | sed 's/,/\n/g'
sed -e 's/$/\n/g' -e 's/,/\n/g' sample.txt
clear
echo linux bob sally | awk '{print $2}'
echo linux bob sally | awk '{print $3,"likes",$1}'
awk -F ',' '{print $1}' sample.txt
awk -F ',' '{print $1}' sample.txt | awk '{print $2 ", " $1}'
cat sample.txt
awk -F ',' '/Dakota/ {print $1}' sample.txt
awk -F ',' '/Dakota/ {print NR,$1}' sample.txt
cat sample.txt | tr ',' '\t'
cat sample.txt | tr 'a-z' 'A-Z'
man tr
cat sample.txt | tr '[:lower:]' '[:upper:]'
```

### Networking and the CLI
- ping - sends msg to host(s)
- ip - the new, better version of ifconfig, can use route within it
- nslookup - basic DNS lookup
- dig - DNS lookup, provides more info, can provide reverse lookup
- netstat - displays network info, current connections and stats
```bash
ping google.com
ping -c 3 google.com
ifconfig
man ifconfig
ip address
ip -s link
ip help
ip address help
ip link help
ip address
sudo ip link set dev enp0s3 down
ip address
ping google.com
sudo ip link set dev enp0s3 up
ip address
ping google.com
ip route
route
sudo ip route add 10.0.3.0/24 via 10.0.2.1
ip route
sudo ip route delete 10.0.3.0/24 via 10.0.2.1
ip route
nslookup google.com
dig google.om
dig -x 8.8.8.8
netstat -at
netstat -at
netstat -lt
Type in separate terminal: python3 -m http.server
netstat -lt
```

### File Transfer Utilities
- scp - secure copy, copies files across network using SSH
- rsync - computes difference between source files and destination files and only transfers the difference
```bash
scp file.txt 192.168.100.4:/home/bob/
Remote host: ls
scp -r files 192.168.100.4:/home/bob/
Remote host: ls
Remote host: ls files/
scp 192.168.100.4:/home/bob/remote-file.txt backup/
scp -r 192.168.100.4:/home/bob/remote-files backup/
scp file.txt sally@<ip>:/home/sally/
rsync -avzh file2.txt 192.168.100.4:/home/bob/
rsync -avzh file2.txt 192.168.100.4:/home/bob/
man rsync
```

### Converting Text Files
- file - verify files have correct line endings
- dos2unix, unix2dos - convert file(s) format
```bash
cd line-endings
ls
file *.txt
vim sample-dos-file.txt
:e ++ff=unix
vim sample-macos-file.txt
cp sample-unix-file.txt temp.txt
unix2dos temp.txt
file temp.txt
unix2dos -n sample-unix-file.txt temp.txt
file temp.txt
cp sample-unix-file.txt temp.txt
unix2dos -c mac temp.txt
file temp.txt
cp sample-dos-file.txt temp.txt
dos2unix temp.txt
file temp.txt
cp sample-macos-file.txt temp.txt
dos2unix -c mac temp.txt
file temp.txt
```

# Text Editors

### Nano
- simple text editor
- https://www.nano-editor.org/

### vim
- more full featured editor
- https://www.openvim.com/

# Process Mgmt

### Process Information
- ps - report snapshot of current processes
- pstree - does not show PIDs, shows hierarchy 
- top - real time view of processes and resources they use
```bash
ps
man ps
ps ax | less -S
ps -e | less -S <separate window>
ps aux | less -S
ps -ef | less -S
man ps
ps -U root -u root u | less -S
ps -eH | less -S
pstree | less -S
top
d
```

### Foreground & Background Processes
- only 1 foreground process can run in a shell at a given time
- can use xeyes to run processes in the background
```bash
xeyes
ls
Ctrl+c
xeyes &
ls
xeyes
Ctrl+Z
jobs
bg
jobs
fg
ls
xclock &
jobs
fg 2
```

### Managing Processes
- processes can be in 2 main states: running and stopped
	- sleeping - when process is idle
	- zombie - remaining processes that weren't killed off
- kill command, sigkill as last resort
```
Managing Processes
man kill
kill -l
xeyes &
ps -ef | grep xeyes
kill <PID>
xeyes &
ps -ef | grep xeyes
kill -9 <PID>
man pkill
xeyes &
xeyes &
pkill xeyes
sleep 10
```

### Scheduling Processes with Crontab & Init.d
- processes can be executed at a specific time using cron
```bash
less /etc/crontab
ll /etc/cron.daily
crontab -e
5 1 2 * * touch /home/bob/cron/crontab-ran.txt
5 1,13 2 * * touch /home/bob/cron/crontab-ran.txt
*/5 * * * * touch /home/bob/cron/crontab-ran.txt
crontab -l
ll /home/bob/cron/crontab-ran.txt
ll /home/bob/cron/crontab-ran.txt
crontab -r
crontab -l
cd /etc/init.d
ls
ls -d /etc/rc*.d
ls -l /etc/rc5.d/
```

# Regular Expressions
- _a string of text that lets you create patterns that help match, locate, and manage text
```regex
^(?=[A-Z0-9][A-Z0-9@._%+-]{5,253}$)[A-Z0-9._%+-]{1,64}@(?:(?=[A-Z0-9-]{1,63}\.)[A-Z0-9]+(?:-[A-Z0-9]+)*\.){1,8}[A-Z]{2,63}$

^(?:[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*|"(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21\x23-\x5b\x5d-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])*")@(?:(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?|\[(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?|[a-z0-9-]*[a-z0-9]:(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21-\x5a\x53-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])+)\])$
```
- 4 primary components: character classes, quantifiers, roots, anchors
- use https://regexr.com/ for expression explanations
- can be used to search for pattern(s) and replace 
- very powerful, not appropriate for all situations - only use when needed
	- regex is greedy
	- don't build an expression all at once
	- test with valid and invalid data
	- add comments using x modifier

# Bash Scripting

### Basics
- series of bash commands that are stored in a file, can be executed by running the script
```bash
bash hello-world.sh
ls -l hello-world.sh
./hello-world.sh
chmod +x hello-world.sh
./hello-world.sh
gvim executing-commands-example.sh &
./executing-commands-example.sh
```

### Control Structures
```bash
gvim if-examples.sh &
./if-examples.sh
gvim comparison-examples.sh
./comparison-examples.sh
gvim case-example.sh &
./case-example.sh 5
./case-example.sh 5.1
```

### Loops
```bash
gvim loop-examples.sh &
./loop-examples.sh | less
```

### Example
- arguments are stored in variables
```bash
gvim command-line-arguments-example.sh &
./command-line-arguments-example.sh first second third fourth fifth 6 7 8 9 10 11 12 13
https://xkcd.com/936/
./generate-password.sh 4 '-'
```




