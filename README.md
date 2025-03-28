# incident-response-playbooks

## Background
Enterprise Incident Response Plan is a standardized, documented, and repeatable process that defines high-level incident agnostic steps that need to be taken to resolve an incident throughout its life cycle. It includes the roles and responsibilities of various stakeholders in case of an incident. The IR Plans also identifies the key technologies and channels of communications to be leveraged during a response and build processes around permissions and escalations.

Incident Response Playbooks supplement the Enterprise IR Plan and provide written guidance for detecting, responding, and recovering from specific cybersecurity incidents. They are meant to guide Incident responders to follow an instructional procedure during an incident. They are living documents and need updates as new threats arise, detection and response tools change.

The primary objective of this assignment is to develop practical skills in creating Incident Response Playbooks tailored to specific cybersecurity scenarios. Students will apply theoretical knowledge to real-world situations, enhancing their understanding of incident response strategies and preparations.

 
## Objective
You are the Incident Response Manager at "Viva la Vita Online”, an online store created in 2022 that sells mostly vitamins and food supplements to individuals and retailers. As part of your responsibilities, you need to document Incident Response playbooks for this organization following the structure included into the annex of this assignment.

For this, you are provided with details on the most important current security controls implemented at "Viva la Vita Online", listed below.

## Network Controls
Perimeter Firewall on the network egress points (Fortinet FortiGate 7.4)
Intrusion Prevention Sensors on the internal network (Suricata 6.0.15)
Email Gateway with Anti-malware Anti-Spam Protection (Symantec Mail Security for Microsoft® Exchange 7.10)
Security Information and Event Management (IBM QRadar 7.5)
Host Controls
Anti-malware Endpoint Protection on all devices (Symantec Endpoint Protection Client for Windows 14.3)
Full Disk Encryption on employee laptops (Bitlocker for Windows 10 and 11 versions)
Other Controls
Vulnerability Patching Management (Tenable Nessus 10.6)
 

## CSIRT composition
Also, the first step you took as an Incident Response Manager was to create the Computer Security Incident Response Team (CSIRT). The CSIRT includes the following role members-

1. Incident Response Manager (You)
2. IT Security Analyst
3. Network and Systems Engineer
4. Application and E-commerce Specialist
5. Legal and Compliance Advisor
6. Communications and Public Relations Coordinator
7. Human Resources Representative
 

## Incident Handling Scenarios
Each of the following scenarios is intended to represent a specific type of scenario, so the playbook you define will be used the next time an scenario like this (or a similar one) happens. Stick to the description of the specific scenario and the description of the organization provided above and take assumptions if you need (these assumptions need to be clearly identified in your playbook "Introduction" section. 

You need to provide playbooks for 2 of the following incident handling scenarios. In order to select which scenarios you need to work with, you need to apply the following bash script:

```
#!/bin/bash
sc1=$(( 10#$1 % 12))
sc2=$(($((10#$1 + 3)) % 12))
echo "Scenarios for NUID $1 are:  $sc1 and $sc2"
Run the script and provide your NUID as an argument.
```

```
./playbooks.sh 0038383838
Scenarios for NUID 0038383838 are:  2 and 5
```

> The previous output is just an example, you need to execute the script with  your own NUID. 

List of numbered scenarios:
Scenario #	Scenario Title	Description
0	Zero-day Vulnerability on the Web Server	The SIEM detected connections to unusual old web server pages. A zero-day vulnerability enabled directory listing, exposing product catalogs and potentially customer order details. The server manufacturer is working on a patch.
1	Unauthorized Access to Payroll Records	The SIEM detected attempts to access payroll records from the account “j.saw” of John Saw in finance, compromised via a social engineering attack. Immediate response actions are unclear.
2	Loss/Stolen Employee’s Laptop	The CIO lost a laptop at a Spanish airport. It was turned off, encrypted with BitLocker, and contained sensitive business strategies and potential product formulas. Remote wipe capabilities and data access risks are unknown.
3	Hashed Passwords Files	Back-up tapes with /etc/passwords and /etc/shadows files from a 2015 Linux database server were stolen, potentially affecting customer and order databases. The current password protection mechanism used then is unknown.
4	SQL Injection Vulnerability	An audit revealed an SQL injection vulnerability in a database application, potentially risking employee data. The application's external accessibility and the last security audit timeframe are unknown.
5	By Default Cloud Service Provider Privileges	Tax information leakage occurred due to “AWS ReadOnlyAccess policy" allowing full read access to S3 buckets shared with a third-party supplier. Immediate actions to restrict access and review third-party contracts are not mentioned.
6	Rogue Wireless Access Point	Employees reported Wi-Fi issues from the cafeteria due to an unauthorized AP. Network security measures and any previous similar incidents are not detailed.
7	Blacklisted IP Seen in VPN Connections	A VPN connection from a blacklisted IP was flagged, using the account “j.saw.” Unauthorized access to internal communications and project management tools is suspected.
8	Rootkit Installed in Development Server	The Slapper Worm rootkit was found in a Linux development server, compromising product development data and internal code repositories. The criticality of data/services on the server and the date of the last security scan are unknown.
9	Data Breach Incident	An email claimed exfiltration of client PII data, demanding 1000 BTC. A large data transfer from an internal database to a known threat actor was confirmed. Previous similar extortion attempts are not mentioned.
10	Zoom Link Leaked	A Zoom link for an executive meeting was mistakenly shared with ex-employees, some now with competitors. Exposure of strategic business discussions and sensitive internal decisions is assumed.
11	Data Exfiltration from an Internal Employee	An employee uploaded customer order histories and personal information to cloud storage and a flash drive during their notice period. Previous suspicions or incidents involving this employee are not mentioned.
 

### Activity Diagram for short-term containment strategy 
Due to the importance of a rapid response, you also need to prepare an activity diagram which provide a clear view of the sequence of activities that need to be taking in order to contain the incident in the short-term. 

Here you have an example for a ransomware attack, where several critical files have been encrypted, and a ransom note demands payment in cryptocurrency. The attack appears to have originated from a phishing email that an employee inadvertently responded to. The affected systems contain sensitive project data and employee information.

 https://www.plantuml.com/plantuml/png/NOynRiCm34LtdOBdQ9UuGOSC3OAc5n3eRqIm9GeabSAthwnksRwW_nx9atbKRtaB8uJmDcrGfqlXDACuVSEg50Fz8ERt_dynsQA3fcK1EsQwx-R85cBf6TmKT9QSMqaSFNLsK8SiBJlTMIf85fhS8w-3EZ_0AttqPwkZVLCOz0dwV1vRC4RjAiCmDN-89a_uDvSUexyCfPkA2yiso2_f9L6wmdz5ruwPImqdbFau_Gy0![image](https://github.com/user-attachments/assets/1f393050-318b-42bb-a42f-e8dea01084ba)


## Sources of information 
To better prepare for responding to these incidents, you will document Incident Response playbooks for your organization. You can see different examples of scenarios and playbooks in:

NIST.SP.800-61r2.pdf Links to an external site.. (Sections 3 and Annex A). This is the most important because the structure of playbook you need to follow is based on this document.
NIST.SP.800-184.pdf Links to an external site.
MITRE Cyber Exercise Playbook Links to an external site.
 

## Deliverables
Submit a pdf document containing:

The output of the execution of your assigned incident scenarios
IR playbooks for the 2 incidents you have been assigned to

Follow the structure provided in the Annex of this assignment.
The document with the two playbooks assigned needs to be between 15 to 20 pages long .
Focus on the technical security architecture provided (such as the existing security controls), and if you need, describe any additional controls assumptions in your "Introduction Section" that adapts to the given scenario. This can include alerts that you have created in your SIEM or additional preventive, detective or corrective controls not listed above.
Each playbook, needs to include the Activity Diagram for Short-term Containment Strategy .
 

## References

NIST Guide Provides Way to Tackle Cybersecurity Incidents with Recovery Plan, Playbook.

https://www.nist.gov/news-events/news/2016/12/nist-guide-provides-way-tackle-cybersecurity-incidents-recovery-plan

This publication provides tactical and strategic guidance regarding the planning, playbook developing, test. 

https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-184.pdf 

Defining CSIRTs

https://www.us-cert.gov/bsi/articles/best-practices/incident-management/defining-computer-security-incident Links to an external site. response-teams Links to an external site.
