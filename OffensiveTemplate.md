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

![nmap_scan](https://user-images.githubusercontent.com/85695649/146116107-ea6cb609-8ed3-4efc-a7a0-046da1c4c69c.png)



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
  ![flag1](https://user-images.githubusercontent.com/85695649/146116156-b394083b-9260-4475-9935-1137144a6da9.png)    
    - **Exploit Used**
      - SSH
      - ssh michael@192.168.1.110 
      - Password: michael
  - `flag2.txt`: `flag2.txt` fc3fd58dcdad9ab23faca6e9a36e581c
    
    ![flag2](https://user-images.githubusercontent.com/85695649/146116328-79eae558-78a4-4812-96c2-12fac27aafd1.png)
    - **Exploit Used**
      - Open HTTP
      - cd /var/www && find -type f -iname *flag2*
