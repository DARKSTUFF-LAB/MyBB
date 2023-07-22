
# MyBB 1.8.33 User CP email persistent XSS

```
- MyBB 1.8.33 User CP email persistent XSS
- Mybb version < 1.8.34 
- Discoverer: Ahmet Altuntaş
- https://github.com/mybb/mybb/security/advisories/GHSA-3q8x-9fh2-v646
```

## Description

Cross-site scripting (XSS) vulnerability in the User CP module allows remote authenticated users to inject HTML via the user email field, triggered on the User CP Home page.

After registration, the e-mail address is changed and the XSS payload is placed. Then, when "User CP" is entered, the vulnerability is triggered.

```
Payload:
"><svg/onload=confirm('CVE')>"@cve.com
```
![img](https://github.com/ahmetaltuntas/CVE-2023-28467/blob/main/1.png?raw=true)


![img](https://github.com/ahmetaltuntas/CVE-2023-28467/blob/main/2.png?raw=true)

## Solution
Upgrade MyBB version 1.8.34 or higher
