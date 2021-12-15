# Red Team: Summary of Operations

## Table of Contents
- Exposed Services
- Critical Vulnerabilities
- Exploitation

### Exposed Services
_TODO: Fill out the information below._

Nmap scan results for each machine reveal the below services and OS details:

```bash
$ nmap -sV 192.168.1.110 
  
```
![nmap](/Users/aaronparson/Desktop/Final/nmap_scan.png)

This scan identifies the services below as potential points of entry:
- Target 1
 - Port 22 
 - Port 80 
 - WordPress



The following vulnerabilities were identified on each target:
- Target 1
  - openssh 
  - Apace HTTP 
  - WordPress



### Exploitation


The Red Team was able to penetrate `Target 1` and retrieve the following confidential data:
- Target 1
  - `flag1.txt`: `flag1.txt` b9bbcb33e11b80be759c4e84
  ![flag1](/Users/aaronparson/Desktop/Final/flag1.png)
    - **Exploit Used**
      - SSH
      - ssh michael@192.168.1.110 
      - Password: michael
  - `flag2.txt`: `flag2.txt` fc3fd58dcdad9ab23faca6e9a36e581c
    ![flag2](/Users/aaronparson/Desktop/Final/flag2.png)
    - **Exploit Used**
      - Open HTTP
      - cd /var/www && find -type f -iname *flag2*