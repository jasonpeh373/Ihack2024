![image](https://github.com/user-attachments/assets/5fbc31ab-b416-41b3-8e1a-b9e2ed54551f)# iHack2024

## Overview

**Team: Bømbåstïç S¡dë £¥€**

![image](https://github.com/user-attachments/assets/92abb8ae-5ee6-462b-ad67-14470dc4f945)<br>

---

### Table of Contents

- [Forensic](#forensic)
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
  - [Splunk-10](#splunk-10)

---

# Forensic

---

## Lock<br>

![image](https://github.com/user-attachments/assets/d06146bc-e439-4bd0-9259-1fa1adf1515e)<br>

1. We need to extract the file.<br>
![image](https://github.com/user-attachments/assets/2d15982d-19e0-405f-ba7b-34518f7f5c88)<br>

2. While examining the `Windows\PowerShell.evtx` file, I discovered a password.<br>
![image](https://github.com/user-attachments/assets/61555adc-ce8d-4ace-88a7-3bb84970901f)<br>

3. Next, I tried to open the `storageM.img` file and used the password I found.<br>
![image](https://github.com/user-attachments/assets/7ac7f50a-5754-4e0d-aa2c-07e941821172)<br>

4. After successfully entering the password, I checked my disks and found a new one named `ihack-data`.<br>
![image](https://github.com/user-attachments/assets/2c1d5f9f-41c2-4132-a501-16930d0e82c6)<br>

5. Finally, I opened the `flag.txt` file on the new disk and retrieved the content.<br>
![image](https://github.com/user-attachments/assets/623108f6-6f20-40a5-b785-450fc034db22)<br>

---

## Splunk-1<br>

![image](https://github.com/user-attachments/assets/8c25d35c-aec6-4eff-988a-15e9f3e1cef6)<br>

1. Upon analyzing the logon events, I discovered that the admin was being attacked by the IP address `192.168.8.41`.<br>
![image](https://github.com/user-attachments/assets/d9c56780-91bb-4ad9-9bdd-51504aab5b39)<br>

2. I searched in the Sysmon host and source IP and found that the host IP is `192.168.8.52`.<br>
![image](https://github.com/user-attachments/assets/06db029d-3bb3-4d7d-b1af-3b94a2f634d9)<br>

3. So I tried the flag in `ihack24{admin:192.168.8.52}`.<br>
![image](https://github.com/user-attachments/assets/146cdebf-2b68-416a-8040-31a95e605ab8)<br>

---

## Splunk-2<br>

![image](https://github.com/user-attachments/assets/ad437409-624a-401c-9de0-672baef0185a)<br>

1. Based on Splunk-1, I found the attacker's IP is `192.168.8.41`, so this is the flag: `ihack24{192.168.8.41}`.<br>
![image](https://github.com/user-attachments/assets/51b36278-80f5-4d1e-8dc2-9bfd5ec32fb5)<br>

---

## Splunk-3<br>

![image](https://github.com/user-attachments/assets/788bee36-a3eb-4c76-b530-69e99737fe9c)<br>

1. I searched for the earliest time for logon.<br>
![image](https://github.com/user-attachments/assets/75c6b808-3914-48a7-ba69-a685a522b6f0)<br>

2. I checked the event to get the time.<br>
![image](https://github.com/user-attachments/assets/20a58706-d2ad-42cf-936a-4635da38cb3e)<br>

3. So the flag is:<br>
![image](https://github.com/user-attachments/assets/c4e41878-891c-4e79-8ae0-74d3a4b98ac9)<br>

---

## Splunk-4<br>

![image](https://github.com/user-attachments/assets/26bfefb4-a44c-46cd-8844-c002dae734e8)<br>

1. I checked the command line.<br>
![image](https://github.com/user-attachments/assets/28542106-9641-4378-8391-802f993aa266)<br>

2. Based on the previous answer, I found a command executed at 09:57:20 PM, which was `systeminfo`.<br>
![image](https://github.com/user-attachments/assets/a0e83baf-953f-4e97-bd83-9ddb6d41c16f)<br>

3. So, I guessed it is the flag:<br>
![image](https://github.com/user-attachments/assets/748c914d-a63d-4ac0-894b-44ea6df9fbd5)<br>

---

## Splunk-5<br>

![image](https://github.com/user-attachments/assets/e61d71ac-4969-428d-b7c3-c298f21113ad)<br>

1. I searched `ExclusionPath` and found the flag.<br>
![image](https://github.com/user-attachments/assets/c680af8b-1d10-4fcc-8df2-9b013221a89d)<br>

2. This is the flag:<br>
![image](https://github.com/user-attachments/assets/6cabc412-8021-4037-9d0a-36ce7e4de27a)<br>

---

## Splunk-6<br>

![image](https://github.com/user-attachments/assets/386395de-bee2-448f-8101-b95ff59bb3ca)<br>

1. When I tried to find Splunk-8, I saw some IP addresses in the payload.<br>
![image](https://github.com/user-attachments/assets/fc1c5d9a-f1fc-43ff-9e9d-37ac8d173743)<br>

2. So, I tried the IP and found it was the flag:<br>
![image](https://github.com/user-attachments/assets/fed3b845-fad6-4c9f-9659-cfb25c63fe93)<br>

---

## Splunk-7<br>

![image](https://github.com/user-attachments/assets/4975f59f-f8c4-459f-8a99-fe27ab07ff28)<br>

1. I searched by IP backdoor: `157.230.33.7`.<br>
![image](https://github.com/user-attachments/assets/10c411af-64b3-43de-b041-1deaa8dcceb6)<br>

2. That is the flag:<br>
![image](https://github.com/user-attachments/assets/e351dc35-7885-498a-8367-cd094fa12da0)<br>

---

## Splunk-8<br>

![image](https://github.com/user-attachments/assets/aa7d216e-1b7e-4f52-9ed4-e2b8aa01d106)<br>

1. I filtered by `ExclusionPath` and `.exe`.<br>
![image](https://github.com/user-attachments/assets/8937bae6-c278-495d-96e4-37c42bfe43b7)<br>

2. So I got the flag: `ihack24{nmap.exe}`.<br>
![image](https://github.com/user-attachments/assets/bd07caa6-db76-407b-8f14-a3e28ce70be5)<br>

---

## Splunk-9<br>

![image](https://github.com/user-attachments/assets/119fe70a-5157-4e24-8605-7589f1a5f8b1)<br>

1. I filtered by event code `4720` and saw a new user created: `operator`.<br>
![image](https://github.com/user-attachments/assets/bd307a86-5cb0-4de9-8d85-f9b4f63c2c28)<br>

2. I filtered by `operator` and saw a password in the PowerShell event: `operator123`.<br>
![image](https://github.com/user-attachments/assets/19f0b15f-8ff7-43e1-a9a3-9692ed9f56d3)<br>

3. This is the flag:<br>
![image](https://github.com/user-attachments/assets/534b0ea4-c7c0-49fd-b803-ad55f1df17e4)<br>

---

## Splunk-10<br>

![image](https://github.com/user-attachments/assets/1d7aff81-cc5e-4166-bd71-adadcf18ca86)<br>

1. I filtered by `reg.exe`.<br>
![image](https://github.com/user-attachments/assets/8319ca85-dd61-4049-9036-1223963e850d)
<br>

2. I saw some commands in the event and found the backdoor IP, so I guessed the command line is the flag.<br>
![image](https://github.com/user-attachments/assets/c69216f1-405b-4a5d-a646-0c43a03a1fcc)<br>

3. This is the flag:<br>
![image](https://github.com/user-attachments/assets/9cf43520-7b6c-43a1-b8ee-57b9eeefed63)<br>


---

# Incident Handling Challenge<br>
___

## SSH Compromised<br>
![image](https://github.com/user-attachments/assets/dcd6ceaa-6734-4eba-a93e-e27fbe66a586)<br>

1. i open the file in noteped and i saw the user sysadmin like try login using the failed password.<br>
   ![image](https://github.com/user-attachments/assets/a29a4527-08d0-4dba-adf9-f4ea38d90167)
2. so i get the flag.
   ![image](https://github.com/user-attachments/assets/5539de6e-d679-4818-bb72-e66272f311ef)

----

# Malware<br>
---
## Just a normal EXE<br>

![image](https://github.com/user-attachments/assets/2afd2267-8f2b-46df-ba9e-cbf8ec450b6c)<br>
1. after download that file ,i extract that file.<br>
![image](https://github.com/user-attachments/assets/64304c21-427d-4b6b-af8a-299f1b05c887)

2. i check the strings in the file.tar and i found something.<br>
![image](https://github.com/user-attachments/assets/2b8f85d9-a456-4fc8-976a-5d9042c94e86)

3.i try to decode it ,and i got the website link<br>
![image](https://github.com/user-attachments/assets/4c28e00d-1381-44be-a1db-884f86a44fd8)


 












