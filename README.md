# linux
## ubuntu file and folder use space
		du -shc *





## IDE== Integrated Device/Drive Eletronics
## SATA== Serial Advanced Technology Attachment
## SCSI== small Computer System Interface
## SAS==Serial Attached SCSI
## SSD==Solid State Drive

##  slot    	IDE		Virtual disk		SATA/SCSI/SAS/SSD/USB
## ----		----	------------		---------------------
##			hd(x)      vd(x)					sd(x)
			
## 1st			hda 		vda						sda
## 2nd			hdb			vdb						sdb


## Types of partition:
	1.Primary Partition
	2.Extended Partition
	3.Logical Partition

## any harddrive maximum 4 primary partition or 3 primary and 1 extended partition.



## windows boot loader NTLDR
## LINUX boot loader GRUB and LILO
## (i).GRUB==Grand Unified BOOT Loader
## (ii).LiLo==Linux Loader

## Installation method:
	(i) .CD
	(ii).USB
	(iii).Network(PXE-Preboot execution Environment)


## Linux installer anaconda
## windows == administrator
## linux===root

## df -hT     where, df=Disk free | h=human readable | T=Type(File System)
## clear   or  ctrl+L  text mode clear
## means root user
## $ means standard user
## tty == terminal type
## chvt <vtno> change virtual terminal
## example: # chvt 3

## (#logout  #exit  #ctrl+d) logout form system
## (#users   #who   #w) active user information

##cal    (calender)
##cal <M> <Y>
##cal <Y>

## calculator:
## bc
## scale=5
## quit

## bc -l

## ipcalc -nmb 192.168.0.0/24

## help linux
## man cal
## man who
## info who

## 		shutdown:							restart:
		1. init 0							1. init 6
		2. pweroff							2. reboot
		3. shutdown -h							3.shutdown -r
			i.e									i.e
			1. shutdown -h now							1. shutdown -r now
			2. shutdown -h 0							2. shutdown -r 0
			3. shutdown -h 15							3. shutdown -r 15
			4. shutdown -h 18.30 							4. shutdown -r 18.30
		4. halt -p							4.ctrl+alt+delet

## shutdown cancel: #shutdown -c

### #pwd     (print working directory)

	#ls							l=long list
	#ls -l							a=all
	#ls -la							R=recursively
	#ls -R
	#ls -l

## #ctrl+c   (any running system stop)

## #cd  (change Directory)
place to current user home:
	#cd
	#cd ~ 
	#cd ~ <user>
	#cd ..
	#cd  <path of Directory>		(#cd /etc)
	#cd -			(1 step back)
	#cd ../..     (parent to parent)

## mkdir(make Directory):

	#mkdir <dir>  (#mkdir abc)
	#mkdir <dir1> <dir2> <dir3> ....<dirN>
	#mkdir "Directory with space"     (#mkdir "audio song")
	#mkdir Directory\ with space      (#mkdir  audio\ song)
	#mkdir dir1/dir2/dir3   -p
	#mkdir song{1.......10}

	#mkdir  pathshala  /tmp/pathshala


## Delet: rm/rmdir(remove Files/Folder)
	#rmdir <dirname>      (blank directory delete)
	#rm <filename>
	#rm <file1> <file2> <file3> .....<fileN>
	#rm -f <file1> <file2>
	#rm -r <dir>     (delete with directory)
	#rm -f <dir>

	#rmdir *  (delete all empty directory)
	#rm -fr * (all file delete)

### touch command used file create and time modify if this file already exist
	#touch {1..5}.txt
	#touch {a..d}.conf

## su(switched user)
	#su - (root user switched)
	#su - <username>

	#uptime   (system up time)

### useradd:
	#useradd <username>
	#useradd -d <home dir> <username>
	#useradd -u <uid> <username>
	#useradd -s <shell> <username>
	#useradd -o -u <uid> <username>
## useradd with comments:
	#useradd -c "comments" <username>
## Example:
	#useradd alex
	#useradd -d /var/alex alex
	#useradd -u 1800 neo
	#useradd -s /sbin/nologin brad
	#useradd -o -u 0 admin
	#usermod -o -u 0 admin
	#useradd -c "mrs fahima" fahima
-------------------------
	
	#yum install finger -y 
	#chfn root
	#finger
	#finger <usename>
	#chfn <username>
	#id

## passwd:
	#passwd
	#passwd <username>
	#passwd -l <username>
	#passwd -u <username>
	#passwd -d <username>

## userdel:
	#userdel <username>      (just user delete)
	#userdel -r <username>    (userdelete with directory)

## Example:
	#userdel alex
	#userdel -r user10

## History
	#history
	#history 10  
	#history -c    (clear history)
	#history -r     (history restore)
	#!<history no>
	#!!              (previous command)
	#!p     (check down to up)

## DATE AND TIME
	#date     (os date and time)
	#hwclock  (bios date and time)

	#date <MMDDHHmmYYYY> 
	#date <MMDDHHmmYYYY.ss>

	where,M=month, D=day, H=hour, m=minute, y=year, s=second

## system to bios time adjust:
	#hwclock --systohc (os to bios)
	#hwclock -w
	#hwclock --hctosys  (bios to os)
	#hwclock -s

## read/view file:
	1. cat
	2. more
	3. less 
	4. head
	5. tail
	6. vi/vim (editor)
	7. nano (editor)
	8. tac   (inverse cat)

	/etc/passwd = user information
	/etc/shadow = password,password and account expire date last password change)


## cat:
	#cat file
	#cat file1,file2........fileN
	q for quit
## more can not scroll and less can scroll

## head:
	#head filename   (by default 10 line)
	#head -n <no of line> filename
	#head -<no of line> filename

## tail: (down to up)
	#tail filename
	#tail -n <no of line> filename
	#tail -<no of line> filename
	#tail -f filename (flow new add show)
	#tailf filename  (flow new add show)

## output redirect(>,>>):
	#date > /root/date.txt     (file create or already file create  so file replace)
	#cal >> /root/date.txt     (file create or already file create  so previous file information and put new information)

	#shift+zz(command mode)

## wc(word count)
	#wc filename
	#wc -w filename
	#wc -l filename
	#wc -c filename

	where, w = word
		l= line
		c=character


## 1    2 3 4  5    6      7
## root:x:0:0:root:/root:/bin/bash		

	1. login name
	2. password (x means password)
	3. uid (user id)
	4. Gid (group id)
	5. user comments
	6. home directory
	7. shell


## vi/vim:
	two types mode 
		1. command mode
		2. insert mode

	#vi filename

	i=immediately insert or insert btn
	a= insert after the cursor
	o=open new line under cursor
	O=open new line up the cursor

	:x! =save and exit
	:wq! =write and quit
	:q! =exit without saving
	:w = write but not quit

#vimdiff command /tmp/file7


## message of the day -motd:
	vi /etc/motd   (normally blank we can set any message)

## virtually line add:
	:set number
	or 
	:set nu

## number remove
	:set nonumber
	or
	:set nonu

	ngg = nth line
	gg= 1st line
	G=last line
	10gg= 10th line
	10G= 10th line
	j= 1 line jump
	3j=3 line jump
	k= 1 line kick
	3k= 3 line kick

	10gg === :10 --10th line
		 : 1 -- 1st line
		 : $ -- last line
		 
## hostname change:
	#hostname <new hostname>  (temporary change)

	#hostnamectl 
	#hostnamectl set-hostname <new hostname>
	or 
	#vi /etc/hostname

## update hostname:
	#bash

## hostname two types 
	1. static
	2. Dynamic

## DHCP types hostname no file

## hostnamectl set-hostname desktop8.example.com


## cp(copy files/ folder):
		#cp <src> <dst>
		#cp /root/class7/commands   /tmp
		    -----(src)---------    -(dst)--
		#cp <src1> <src2> <src3> ...<srcN> <dst>	
		#cp /etc/motd  /etc/passwd   /tmp
	        	(src1)      (src1)     -(dst)-
## folder copy just -r add
	#cp -v <src>  <dst>
	#cp -f <src>  <dst>
	#cp -p <src>  <dst>

	where, v=verbose
		f=forcely
		p=preserve
		
	#cp -pvf <src> <dst>

## Directory copy:
	#cp -fr <src dir>   <dst dir>


## mv(move/ rename):
	#mv <current name> <new name>
	#mv   abc	abc.old
	#mv <src>  <dst>
	#mv  /root/abc   /tmp     (cut--paste)
	#mv  /root/abc   /tmp/abc.old (move & rename)
-----------------------------------------------------------------------------------------------------------------


	IDE== Integrated Device/Drive Eletronics
	SATA== Serial Advanced Technology Attachment
	SCSI== small Computer System Interface
	SAS==Serial Attached SCSI
	SSD==Solid State Drive

	slot    	                 IDE			Virtual disk		      SATA/SCSI/SAS/SSD/USB
	----		               ----	                ------------		-------------------------------
					hd(x)                     vd(x)					sd(x)
			
		1st			hda	                   vda					sda
		2nd			hdb	                   vdb					sdb


## Types of partition:
		1.Primary Partition
		2.Extended Partition
		3.Logical Partition

## Any harddrive maximum 4 primary partition or 3 primary and 1 extended partition.

	windows boot loader NTLDR
	LINUX boot loader GRUB and LILO
		(i).GRUB==Grand Unified BOOT Loader
		(ii).LiLo==Linux Loader

## Installation method:
	(i) .CD
	(ii).USB
	(iii).Network(PXE-Preboot execution Environment)

## Linux installer anaconda
## windows == administrator
## linux===root

	#df -hT     where, df=Disk free | h=human readable | T=Type(File System)
	#clear   or  ctrl+L  text mode clear
	# means root user
	$ means standard user
	tty == terminal type
	chvt <vtno> change virtual terminal
	example: # chvt 3

	(#logout  #exit  #ctrl+d) logout form system
	(#users   #who   #w) active user information

	#cal    (calender)
	#cal<M><Y>
	#cal<Y>
## calculator:
	#bc
	scale=5
	quit
	#bc -l
	#ipcalc -nmb 192.168.0.0/24
## help linux
	#man cal
	#man who
	#info who

			
## shutdown cancel: 
	#shutdown -c
	
## #pwd     (print working directory)
		#ls							l=long list
		#ls -l							a=all
		#ls -la							R=recursively
		#ls -R
		#ls -l

		#ctrl+c   (any running system stop)

		#cd  (change Directory)
		place to current user home:
		#cd
		#cd ~ 
		#cd ~ <user>
		#cd ..
		#cd <path of Directory>		(#cd /etc)
		#cd -			(1 step back)
		#cd ../..     (parent to parent)

## mkdir(make Directory):
		#mkdir<dir>  (#mkdirabc)
		#mkdir<dir1><dir2><dir3> ....<dirN>
		#mkdir "Directory with space"     (#mkdir "audio song")
		#mkdir Directory\ with space      (#mkdir  audio\ song)
		#mkdir dir1/dir2/dir3   -p
		#mkdir song{1.......10}

		#mkdir pathshala  /tmp/pathshala


## Delet: rm/rmdir(remove Files/Folder)
		#rmdir <dirname>      (blank directory delete)
		#rm <filename>
		#rm <file1><file2><file3> .....<fileN>
		#rm -f  <file1><file2>
		#rm -r  <dir>     (delete with directory)
		#rm –f  <dir>

		#rmdir *  (delete all empty directory)
		#rm -fr * (all file delete)

## touch command used file create and time modify if this file already exist
		#touch {1..5}.txt
		#touch {a..d}.conf

## su(switched user)
		#su - (root user switched)
		#su - <username>

		#uptime   (system up time)

## useradd:
	#useradd <username>
	#useradd -d <home dir><username>
	#useradd -u <uid><username>
	#useradd -s <shell><username>
	#useradd -o -u <uid><username>
## useradd with comments:
	#useradd -c "comments" <username>
## Example:
	#useradd alex
	#useradd -d /var/alexalex
	#useradd -u 1800 neo
	#useradd -s /sbin/nologin brad
	#useradd -o -u 0 admin
	#usermod -o -u 0 admin
	#useradd -c "mrsfahima" fahima

-----------------------------------------------------
	#yum install finger -y 
	#chfn root
	#finger
	#finger <usename>
	#chfn<username>
	#id

## passwd:
	#passwd
	#passwd<username>
	#passwd -l <username>
	#passwd -u <username>
	#passwd -d <username>

## userdel:
	#userdel <username>      (just user delete)
	#userdel -r <username>    (userdelete with directory)

## Example:
	#userdel alex
	#userdel -r user10

## History
	#history
	#history 10  
	#history -c    (clear history)
	#history -r     (history restore)
	#!<history no>
	#!!              (previous command)
	#!p     (check down to up)

## Date and Time
	#date     (os date and time)
	#hwclock  (bios date and time)

	#date <MMDDHHmmYYYY>
	#date <MMDDHHmmYYYY.ss>

	where,M=month, D=day, H=hour, m=minute, y=year, s=second

## system to bios time adjust:
	#hwclock --systohc (os to bios)
	#hwclock -w
	#hwclock --hctosys  (bios to os)
	#hwclock -s

	read/view file:
	1. cat
	2. more
	3. less 
	4. head
	5. tail
	6. vi/vim (editor)
	7. nano (editor)
	8. tac   (inverse cat)

	/etc/passwd = user information
	/etc/shadow = password,password and account expire date last password change)

## cat:
	#cat file
	#cat file1,file2........fileN
	q for quit
	more can not scroll and less can scroll

## head:
	#head filename   (by default 10 line)
	#head -n <no of line> filename
	#head -<no of line> filename

## tail: (down to up)
	#tail filename
	#tail -n <no of line> filename
	#tail -<no of line> filename
	#tail -f filename (flow new add show)
	#tailf filename  (flow new add show)
	
	output redirect(>,>>):
	#date  >  /root/date.txt     (file create or already file create  so file replace)
	#cal>>  /root/date.txt     (file create or already file create  so previous file information and put new information)

	#shift+zz(command mode)
	#wc(word count)
	#wc filename
	#wc -w filename
	#wc -l filename
	#wc -c filename
	where, w = word
		l= line
		c=character
	1    2 3 4  5    6      7
	root:x:0:0:root:/root:/bin/bash		
	1. login name
	2. password (x means password)
	3. uid (user id)
	4. Gid (group id)
	5. user comments
	6. home directory
	7. shell


	vi/vim:
	two types mode 
	1. command mode
	2. insert mode

	#vi filename

	i=immediately insert or insert btn
	a= insert after the cursor
	o=open new line under cursor
	O=open new line up the cursor

	:x! =save and exit
	:wq! =write and quit
	:q! =exit without saving
	:w = write but not quit

	#vimdiff command /tmp/file7


	message of the day -motd:
	#vi /etc/motd   (normally blank we can set any message)

### virtually line add:
	:set number
	or 
	:set nu

### number remove
	:set nonumber
	or
	:set nonu

	ngg = nth line
	gg= 1st line
	G=last line
	10gg= 10th line
	10G= 10th line
	j= 1 line jump
	3j=3 line jump
	k= 1 line kick
	3k= 3 line kick

	10gg === :10 --10th line
			 : 1 -- 1st line
			 : $ -- last line
		
### hostname change:
	#hostname <new hostname>  (temporary change)
	#hostnamectl
	#hostnamectl set-hostname <new hostname>
	or 
	#vi /etc/hostname
### update hostname:
	#bash

### hostname two types 
	1. static
	2. Dynamic

### DHCP types hostname no file
### hostnamectl set-hostname desktop8.example.com

### cp(copy files/ folder):
	#cp<src><dst>
	#cp /root/class7/commands   /tmp
	    -----(src)---------    -(dst)--
	#cp<src1><src2><src3> ...<srcN><dst>	
	#cp /etc/motd  /etc/passwd   /tmp
	     (src1)      (src1)     -(dst)-

# folder copy just -r add
	#cp -v <src> <dst>
	#cp -f <src> <dst>
	#cp -p <src> <dst>

	where, v=verbose
		f=forcely
		p=preserve
		
	#cp -pvf <src> <dst>

### directory copy:
	#cp -fr <srcdir> <dstdir>


## mv(move/ rename):
# mv <current name><new name>
		#mv  abc		abc.old
		#mv <src><dst>
		#mv  /root/abc   /tmp     (cut--paste)
		#mv  /root/abc   /tmp/abc.old (move & rename)

				

	#Yum install bind
	#Yum remove bind
	#Yum update bind
	#Cd /etc/yum.repos.d/
	#Vim abc.repo
	[name]
	Name=
	Baseurl=file:///abc
	Enabled=1
	Gpgcheck=0

	#yum clean all
	#yum repolist
	#yum remove
	#yum update



## Rpm package install
	#rpm -qa
	#rpm -qa | grep bind 
	#rpm -ivh bind….repo
	#rpm -uvh bind
	#rpm -evh bind…repo
	#uname -r


	#cd /etc/sysconfig/network-scripts
	#Vim ifcfg-eth0
	Name=linux
	Bootproto=none/static
	Onboot=yes
	Ipaddr=172.25.1.10
	Gateway=172.25.1.1
	Prefix=24
	Dns1=8.8.8.8
	Dns2=4.4.4.4 

	#Systemctl restart network
	#Systemctl enable network

	#vim /etc/resolve.conf
	#vim /etc/hosts
	#vim /etc/chrony.conf
	#systemctl restart chronyd
