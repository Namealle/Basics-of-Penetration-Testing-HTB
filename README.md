# Basics-of-Penetration-Testing-HTB
writeups from Hack the Box
ping {target IP}
sudo nmap {target IP} to see on which port FTP runs
sudo nmap -sV {traget IP} detect the version and same as just nmap
sudo apt install ftp -y y is used to accept installation without intteraptinng the process
ftp -? to seee what the servise is capable off
ftp {target_IP}
username {anonymous} passowrd {anon123} allow to access FTP services like any other outhenticated user.
you can use {help} to get list of command that you can use.
use ftp>ls or cd to access the folder.
get flag.txt to download the fiel
ftp>bye
