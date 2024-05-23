# Implementing a SOC and Honeynet in Azure

In this security lab project, my aim was to establish a controlled environment for simulating and detecting cyber attacks. My primary focus was on ingesting and analyzing logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. By utilizing OSINT, I created threat maps to help identify geographical attack locations, which could be further leveraged to enhance security posture. This hands-on experience was crafted to deepen my understanding of network security, attack patterns, and defensive strategies.
### Skills Learned

- Proficiency in managing and utilizing Security Information and Event Management (SIEM) systems for collecting, correlating, and analyzing security event data.
- Ability to parse, interpret, and derive insights from logs generated by various network devices and systems, enhancing understanding of system behavior and potential security issues.
- Ability to create and utilize threat maps to visualize potential attack locations and identify geographical patterns, aiding in enhancing security posture.
- Practical experience gained through hands-on engagement with security tools, systems, and methodologies, enhancing overall proficiency in cybersecurity practices and techniques.

### Tools Used

- Security Information and Event Management (SIEM) System: Centralized platform for ingesting, correlating, and analyzing security event data from various sources.
- Telemetry generation tools to create realistic network traffic and attack scenarios.
- Open Source Intelligence (OSINT) used for gathering and analyzing publicly available data such as IP address source location to identify potential threats and vulnerabilities.

## Steps
![image](https://github.com/TyDusseau/SecurityLab/assets/168771739/aaa40d33-31a5-4832-8f49-def0b8e39f2c)
_Ref 1: Created resource group with all necessary components_


![image](https://github.com/TyDusseau/SecurityLab/assets/168771739/666b29a3-b6b4-4e3f-b7ec-1bc4516bc8b9)

_Ref 2: Opened firewall on Azure to allow pings and other brute force attacks_


![image](https://github.com/TyDusseau/SecurityLab/assets/168771739/bce5f1c8-9427-494d-8d77-46c0e019e703)
_Ref 3: Azure log analytics workspace setup to injest logs from honeypot VM with geographical data_


![image](https://github.com/TyDusseau/SecurityLab/assets/168771739/b3662f0b-cefd-4cf2-964e-fb0cb499af14)

_Ref 4: Observed Windows Event Viewer logs to verify Event ID: 4625 (failed logon)_


![image](https://github.com/TyDusseau/SecurityLab/assets/168771739/2ec8b1db-3ccf-4320-a3c6-8c5448af70a9)

_Ref 5: Turning off firewall on VM to allow all traffic and allowing it to become discoverable_


![image](https://github.com/TyDusseau/SecurityLab/assets/168771739/784af483-8dac-4dc8-83b9-72754c406c96)

_Ref 6: Running PowerShell script to output geographical data tied to failed logon attempts (Event ID: 4625) to a log file to be injested by Azure LAW/Sentinel_


![image](https://github.com/TyDusseau/SecurityLab/assets/168771739/106e3f54-926d-4a6e-8044-bcf08c870d75)
_Ref 7: Utilizing OSINT to assist the above PowerShell script in finding locations based on IP address_


![image](https://github.com/TyDusseau/SecurityLab/assets/168771739/dcea8c53-f674-449b-bd71-ac6ce6f24f84)
_Ref 8: Setting up threat map in Sentinel to visualize logs in a geographical map, color-coded by number of attacks per IP/location_


![image](https://github.com/TyDusseau/SecurityLab/assets/168771739/7c580e6b-78df-4cd4-aed8-ff17f564b768)
_Ref 9: Close-up of map for easier viewing_
