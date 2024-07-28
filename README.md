# iHack2024

## Overview

**Team:Bømbåstïç S¡dë £¥€**

![image](https://github.com/user-attachments/assets/92abb8ae-5ee6-462b-ad67-14470dc4f945)<br>

---
### Table of content

- [Forensic](#Forensic)
  - [Lock](#lock)
  - [Splunk-1](#splunk-1)
  - [Splunk-2](#splunk-2)
  - [Splunk-3](#splunk-3)
  - [Splunk-4](#splunk-4)
  - [Splunk-5](#splunk-5)
  - [Splunk-6](#splunk-6)
  - [Splunk-7](#splunk-7)
  - [Splunk-8](#splunk-8)
  - [Splunk-9](#splunk-9)
  - [Splunk-10](#splunk-20)




---
# Forensic <br>
---
## LOCK<br>

![image](https://github.com/user-attachments/assets/d06146bc-e439-4bd0-9259-1fa1adf1515e)

1. we need to ectract the file 
![image](https://github.com/user-attachments/assets/2d15982d-19e0-405f-ba7b-34518f7f5c88)

2. While examining the Windows\PowerShell.evtx file, I discovered a password.
![image](https://github.com/user-attachments/assets/61555adc-ce8d-4ace-88a7-3bb84970901f)

3. Next, I tried to open the storageM.img file and used the password I found.
![image](https://github.com/user-attachments/assets/7ac7f50a-5754-4e0d-aa2c-07e941821172)

4. After successfully entering the password, I checked my disks and found a new one named ihack-data.
![image](https://github.com/user-attachments/assets/2c1d5f9f-41c2-4132-a501-16930d0e82c6)

5.Finally, I opened the flag.txt file on the new disk and retrieved the content.
![image](https://github.com/user-attachments/assets/623108f6-6f20-40a5-b785-450fc034db22)

---
## Splunk-1<br>

![image](https://github.com/user-attachments/assets/8c25d35c-aec6-4eff-988a-15e9f3e1cef6)

1.Upon analyzing the logon events, I discovered that the admin was being attacked by the IP address 192.168.8.41.
![image](https://github.com/user-attachments/assets/d9c56780-91bb-4ad9-9bdd-51504aab5b39)

2. i try search in sysmon host and sourceIp i find that host  ip  is 192.168.8.52
![image](https://github.com/user-attachments/assets/06db029d-3bb3-4d7d-b1af-3b94a2f634d9)

3.so i try the flag in ihack24{admin:192.168.8.52}.

![image](https://github.com/user-attachments/assets/146cdebf-2b68-416a-8040-31a95e605ab8)

---
## Splunk-2<br>

![image](https://github.com/user-attachments/assets/ad437409-624a-401c-9de0-672baef0185a)

1.based on splunk-1 i found the attacker up is 192.168.8.41,so this is the flag:ihack24{192.168.8.41}.
![image](https://github.com/user-attachments/assets/51b36278-80f5-4d1e-8dc2-9bfd5ec32fb5)

---
## Splunk-3 <br>

![image](https://github.com/user-attachments/assets/788bee36-a3eb-4c76-b530-69e99737fe9c)

1.I search the earlist(time) for logon. 
![image](https://github.com/user-attachments/assets/75c6b808-3914-48a7-ba69-a685a522b6f0)

2.I check for the event get the time.
![image](https://github.com/user-attachments/assets/20a58706-d2ad-42cf-936a-4635da38cb3e)

3.So the flag is. <br>
![image](https://github.com/user-attachments/assets/c4e41878-891c-4e79-8ae0-74d3a4b98ac9)

---
## Splunk-4 <br>
![image](https://github.com/user-attachments/assets/26bfefb4-a44c-46cd-8844-c002dae734e8)

1.i check in command line 
![image](https://github.com/user-attachments/assets/28542106-9641-4378-8391-802f993aa266)

2.based on previous answer i just get a time on 09:57:20 PM have execute the command is systeminfo.<br> 
![image](https://github.com/user-attachments/assets/a0e83baf-953f-4e97-bd83-9ddb6d41c16f)

3.so guess is it the flag.<br>
![image](https://github.com/user-attachments/assets/748c914d-a63d-4ac0-894b-44ea6df9fbd5)

---
## Splunk-5 <br>

![image](https://github.com/user-attachments/assets/e61d71ac-4969-428d-b7c3-c298f21113ad)

1.i search ExclusionPath and i found the flag<br>
![image](https://github.com/user-attachments/assets/c680af8b-1d10-4fcc-8df2-9b013221a89d)

2.this is the flag<br>
![image](https://github.com/user-attachments/assets/6cabc412-8021-4037-9d0a-36ce7e4de27a)

---
## Splunk-6 <br>
![image](https://github.com/user-attachments/assets/386395de-bee2-448f-8101-b95ff59bb3ca)

1.when i try to find the splunk-8 i saw there have some ip in the payload
![image](https://github.com/user-attachments/assets/fc1c5d9a-f1fc-43ff-9e9d-37ac8d173743)

2. so i try the the ip  and that is the flag<br>
![image](https://github.com/user-attachments/assets/fed3b845-fad6-4c9f-9659-cfb25c63fe93)

---
## Splunk -7<br>
![image](https://github.com/user-attachments/assets/4975f59f-f8c4-459f-8a99-fe27ab07ff28)

1.i search by ip backdoor :157.230.33.7<br>
![image](https://github.com/user-attachments/assets/10c411af-64b3-43de-b041-1deaa8dcceb6)

2.that is the flag.<br>
![image](https://github.com/user-attachments/assets/e351dc35-7885-498a-8367-cd094fa12da0)

---
## Splunk-8<br>

![image](https://github.com/user-attachments/assets/aa7d216e-1b7e-4f52-9ed4-e2b8aa01d106)

1.i filter by ExclusionPath and .exe
![image](https://github.com/user-attachments/assets/8937bae6-c278-495d-96e4-37c42bfe43b7)<br>
2.so i get the flag is ihack24{nmap.exe}<br>
![image](https://github.com/user-attachments/assets/bd07caa6-db76-407b-8f14-a3e28ce70be5)<br>

---
## Splunk-9 <br>

![image](https://github.com/user-attachments/assets/119fe70a-5157-4e24-8605-7589f1a5f8b1)<br>
1.i filter by eventcode "4720"  and i saw a new user created :operator.<br>
![image](https://github.com/user-attachments/assets/bd307a86-5cb0-4de9-8d85-f9b4f63c2c28)<br>
2.i filter by operator and i saw password in the event powershell "operator123" <br>
![image](https://github.com/user-attachments/assets/19f0b15f-8ff7-43e1-a9a3-9692ed9f56d3)<br>
3.this is the flag.<br>
![image](https://github.com/user-attachments/assets/534b0ea4-c7c0-49fd-b803-ad55f1df17e4)<br>

---

## Splunk-10<br>

![image](https://github.com/user-attachments/assets/1d7aff81-cc5e-4166-bd71-adadcf18ca86)

1.i filter by reg.exe<br>
![image](https://github.com/user-attachments/assets/e68afe42-6f39-442e-a2f1-092e0345cfba)

2.i saw some command in the event and i saw the backdoor ip so i guess that commandline is the flag <br>
![image](https://github.com/user-attachments/assets/c69216f1-405b-4a5d-a646-0c43a03a1fcc)

3. this is the flag<br>
![image](https://github.com/user-attachments/assets/9cf43520-7b6c-43a1-b8ee-57b9eeefed63)<br>

---














