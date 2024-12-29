# INE-Footprinting-and-Scanning-CTF1
A CTF in the eLearnSecurity Junior Penetration Testing assessments

Images for the CTF can be found here: 

# Footprinting and Scanning CTF1 (INE)

As part of my eJPT learning journey on the INE platform, I tackled this CTF focused on footprinting and scanning methodologies. Below is a summary of the steps I took and flags I captured:

# Flag 1: Initial Reconnaissance 
- cat /etc/hosts  
- nmap -sVC -sS -O target.ine.local
The Nmap scan revealed multiple open ports and their services.

# Flag 2: Port 80 Exploration
Navigating to the web server, I discovered hidden paths:
- /robots.txt
- /secret-info/
- /secret-info/flag.txt

# Flag 3: FTP Anonymous Login
The Nmap results showed that FTP allowed anonymous access. Upon connecting, I downloaded several files.

# Flag 4: SQL Credentials
One of the files contained credentials for the SQL service:
- cat creds.txt  
- mysql -u db_admin -p -h target.ine.local  
