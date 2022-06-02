# Google Dorks: InfoSec & Pentesting

Popular Google dorks used in InfoSec and penetration testing. 


**Subdomains** - Find subdomains of a given domain, excluding `www`.
```
site:*.domain.com -www
```

**HTTP** - Find sites without `https`
```
site:pizzahut.com -inurl:https after:2021
intitle:"index of" -inurl:https after:2021
site:*pizzahut.com intitle:"index of" -inurl:https
```

***User Credentials in Log Files***
```
allintext:username filetype:log
```

**CWD** - On Linux `proc` is a file system that contains a hierarchy of special files which represent the current state of the kernel — allowing applications and users to peer into the kernel's view of the system. 
```
inurl:"/proc/self/cwd"
```

**FTP** - Find FTP servers 
```
intitle:"index of" inurl:ftp
```

**Webcams** - Find webcams via the specific string exposed to Google if camera is connected to the Internet with no restrictions.
```
allintitle:"webcamxp 5"
```


**Database Credentials**
```
db_password filetype:env
as_q=db_password
&as_qdr=y
&as_filetype=env
```

**Sites hosted on GitHub**
```
filetype:inc php -site:github.com -site:sourceforge.net
```

**PHP Variables**
```
"Notice: Undefined variable: data in" -forum filetype:php
as_q=
&as_epq=Notice%3A+Undefined+variable%3A+data+in
&as_eq=forum
&as_qdr=y
&as_filetype=php
```

**Apache Server Configuration**
```
intitle:"WAMPSERVER homepage" "Server Configuration" "Apache Version"
```

**H**
```
("qa")
```

