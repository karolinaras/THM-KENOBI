# THM-KENOBI
In this resporitory I would like to present the results of my work on the Try Hack me website. 
>**TryHackMe Kenobi Room** 

#Task 1 
Using *nmap* I scan ip 10.10.137.110 and I found 7 open ports. 

#Task 2
Using nmap command : nmap -p 445 --script=smb-enum-shares.nse,smb-enum-users.nse 10.10.137.110 I found 3 shares.

#Task 3
Using comand: smbclient //10.10.137.110/anonymous I found list the files on the share. (file log.txt)

#Task 4
Using the command: smbget -R smb://10.10.137.110/anonymous I get file 'log.txt' and then I can open it. In this file is information about FTP is running on 21 port.

#Task 5
Using nmap comannd: nmap -p 111 --script=nfs-ls,nfs-statfs,nfs-showmount 10.10.137.110 I found mount */var*

#Task 6
The version of ProFtpd is 1.3.5 and in exploit-db.com  website has 4 exploits. 

#Task 7
Exploit description talks about using SITE CPFR and SITE CPTO commands that are implemented in the mod_copy module. I can use these commands to copy files from the filesystem with an unauthenticated client.


