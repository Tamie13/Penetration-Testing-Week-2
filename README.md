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

  - The name of the script or Metasploit module used: `The exploit/windows/http/icecast_header` allows an attacker or threat actor to gain remote control of a victims system by exploiting a buffer overflow which overwrites the memory on the vicitms system using the "icecast" flaw.  The flaw allows for writing past the end of a pointer array when receiving information greater than 32 characters (headers).

* Vulnerability Explanation:

  -  If you use audio streaming services like `Spotify` then you've used `Icecast.` It is a streaming media server used by radio stations, online music streaming and other similar platforms that allow you to create list of your favorite music and listen to it anywhere at anytime.  The `Icecast Flaw` is used by attackers and or threat actors to inject malicious code into the `Icecast` overflow buffer.  The `Icecast` server has a maximum set of 32 characters in the client's HTTP request.  If the request is longer than 32 characters (aka headers) then the excess is sent to the stack overflow where it fills the buffers allocated for the overflow.  In this process of buffer overflow is something called an `Extended Instruction Pointer (EIP)` that holds the memory address of the next instruction to execute in the buffer overflow.  It is in the `EIP` that an attack is able to be executed.  Once the overflow fills the buffers allocated it overwrites the `EIP` address space.  If it overwrites with a new `return pointer` it can tell the CPU to go to anaddress which contains `instruction code` which will then be executed.  It is here where a malicious code or unwanted process can be executed by an attacker.
  
[Click Here For Full Extract On Information Above](https://www.giac.org/paper/gcih/687/remote-exploitation-icecast-201-server/106910)
  

* Severity:
In your expert opinion, how severe is this vulnerability?
  
The severity of this attack according to CVE was scored at `7.5` highlighting that the compromise of confidentiality, integrity and availabitlity is considerable.
  
[Click Here For CVE Details](https://www.cvedetails.com/cve/CVE-2004-1561/)

*Proof of Concept:
This is where you show the steps you took. Show the client how you exploited the software services. Please include screenshots.



There should be a separate finding for each vulnerability found.









3.	Recommendations

What recommendations would you give to GoodCorp?


