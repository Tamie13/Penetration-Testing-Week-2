<div align="center">GoodSecurity Penetration Test Report

TamieBoychuk@GoodSecurity.com

29 March 2022



<div align="left">

**1.	High-Level Summary**

GoodSecurity was tasked with performing an internal penetration test on GoodCorp’s CEO, Hans Gruber. An internal penetration test is a dedicated attack against internally connected systems. The goal of this test is to perform attacks similar to those of a hacker and attempt to infiltrate Hans’ computer to determine if it is at risk. GoodSecurity’s overall objective was to exploit any vulnerable software, find a secret recipe file on Hans’ computer, and report the findings back to GoodCorp.
The internal penetration test found several alarming vulnerabilities on Hans’ computer: When performing the attacks, GoodSecurity was able to gain access to his machine and find the secret recipe file by exploiting two programs with major vulnerabilities. The details of the attack are below.

  
**2.	Findings**

* Machine IP:
  
  - Machine’s IP address = `192.168.0.20`
  
* Hostname:

  - Actual name of the machine = `MSEDGEWIN10`

* Vulnerability Exploited:

  - The name of the script or Metasploit module used: `The exploit/windows/http/icecast_header` allows an attacker or threat actor to gain remote control of a victims system by exploiting a buffer overflow by overwriting the memory on the vicitms system using the "icecast" flaw.  The flaw allows for writing past the end of a pointer array when receiving 32 HHTP headers.

* Vulnerability Explanation:
Explain the vulnerability as best you can by explaining the attack type (i.e. is it a heap overflow attack, buffer overflow, file inclusion, etc.) and briefly summarize what that attack is. You may need to do extra research online. exploit/windows/http/icecast_header

* Severity:
In your expert opinion, how severe is this vulnerability?

*Proof of Concept:
This is where you show the steps you took. Show the client how you exploited the software services. Please include screenshots.



There should be a separate finding for each vulnerability found.









3.	Recommendations

What recommendations would you give to GoodCorp?



![image](https://user-images.githubusercontent.com/93218323/160717386-262c052a-ee7b-4759-89e4-4b8830337577.png)
