## Week 16 Homework Submission File: Penetration Testing 1

#### Step 1: Google Dorking


- Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is: Karl Fitzgerald

- How can this information be helpful to an attacker:This information can be used in a social engineering campaign.



#### Step 2: DNS and Domain Discovery

Enter the IP address for `demo.testfire.net` into Domain Dossier and answer the following questions based on the results:

  1. Where is the company located: Sunnyvale, CA

  2. What is the NetRange IP address: 65.61.137.64 - 65.61.137.127
  
  3. What is the company they use to store their infrastructure: Rackspace Backbone Engineering

  4. What is the IP address of the DNS server: 65.61.137.117
  
#### Step 3: Shodan

- What open ports and running services did Shodan find: 80, 43, 8080

#### Step 4: Recon-ng

- Install the Recon module `xssed`. 
- Set the source to `demo.testfire.net`. 
- Run the module. 

Is Altoro Mutual vulnerable to XSS: Yes, one vunerability found.

### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

- Command for Zenmap to run a service scan against the Metasploitable machine: nmap -sV -sC -oN 192.168.0.10
 
- Bonus command to output results into a new text file named `zenmapscan.txt`:

- Zenmap vulnerability script command: nmap -sV -sC -oN zenmapscan.txt 192.168.0.10
  
  Use Zenmap's scripting engine to identify a vulnerability associated with the service running on the 139/445 port from your previous scan.
- Once you have identified this vulnerability, answer the following questions for your client:
  
  1. What is the vulnerability: Samba since version 3.5.0 and before 4.6.4, 4.5.10 and 4.4.14 is vulnerable to remote code execution vulnerability.
  
  2. Why is it dangerous: It allows a malicious client to upload a shared library to a writable share, and then cause the server to load and execute it.

  3. What mitigation strategies can you recommendations for the client to protect their server: Use a firewall to protect ports 139/445

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  

