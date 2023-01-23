# THM-KENOBI
In this resporitory I would like to present the results of my work on the Try Hack me website. 
>**TryHackMe Kenobi Room** 

#Task 1 
Using *nmap* I scan ip 10.10.137.110 and I found `7 open ports`. 

![This is an image](https://github.com/karolinaras/THM-KENOBI/blob/fa47a9da1a6b110af85006f070fba73bda76f697/KENOBI1.png)


#Task 2
Using nmap command : nmap -p 445 --script=smb-enum-shares.nse,smb-enum-users.nse 10.10.137.110 I found` 3 shares`.

![This is an image](https://github.com/karolinaras/THM-KENOBI/blob/fa47a9da1a6b110af85006f070fba73bda76f697/KENOBI2.png)


#Task 3
Using comand: smbclient //10.10.137.110/anonymous I found list the files on the share. `(file log.txt)`

![This is an image](https://github.com/karolinaras/THM-KENOBI/blob/fa47a9da1a6b110af85006f070fba73bda76f697/KENOBI3.png)


#Task 4
Using the command: smbget -R smb://10.10.137.110/anonymous I get file `log.txt` and then I can open it. In this file is information about FTP is running `on 21 port`.

![This is an image](https://github.com/karolinaras/THM-KENOBI/blob/fa47a9da1a6b110af85006f070fba73bda76f697/KENOBI4.png)


#Task 5
Using nmap comannd: nmap -p 111 --script=nfs-ls,nfs-statfs,nfs-showmount 10.10.137.110 I found mount `*/var*`

![This is an image](https://github.com/karolinaras/THM-KENOBI/blob/fa47a9da1a6b110af85006f070fba73bda76f697/KENOBI5.png)


#Task 6
The version of `ProFtpd is 1.3.5` and in exploit-db.com  website has `4 exploits`. 

![This is an image](https://github.com/karolinaras/THM-KENOBI/blob/fa47a9da1a6b110af85006f070fba73bda76f697/KENOBI6.png)

and Exploit Database
![This is an image](https://github.com/karolinaras/THM-KENOBI/blob/fa47a9da1a6b110af85006f070fba73bda76f697/KENOBI7.png)


#Task 7
Exploit description talks about using SITE CPFR and SITE CPTO commands that are implemented in the mod_copy module. I can use these commands to copy files from the filesystem with an unauthenticated client.

![This is an image](https://github.com/karolinaras/THM-KENOBI/blob/fa47a9da1a6b110af85006f070fba73bda76f697/KENOBI8.png)


