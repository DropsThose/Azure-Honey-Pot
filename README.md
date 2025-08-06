# Azure Honey Pot Project 

<img width="1477" height="805" src="https://github.com/user-attachments/assets/0f70b68e-be4f-4c57-9b68-bb649b0fa4ee" />

# Introduction
In this project, I created a honeypot utilizing Microsoft Azure. The purpose of this project is to show the risk of having an insecure machine open to the internet and how a properly secured machine can greatly reduce the attack surface. Logs from my VM were centrally located within the Log Analytics Workspace. Microsoft Sentinel was used to generate an attack map, utilizing IP data from the logs to identify the source of malicious traffic globally. 

This project has two parts:

_**Unsecure Environment:**_ The Azure NSG firewall will be set to allow all traffic in, and the host-based firewall will be disabled. OS will be a barebones install with no updates.

_**Secure Environment:**_ As per the recommendations of NIST SP 800-125B, the Azure NSG firewall will be configured following a zero-trust model, only allowing connections from my IP. The host-based firewall will be enabled. Following the recommendations of NIST SP 800-125 for guest operating systems, the VM will be fully updated. 

The environment will be run for 24 hours in each of these states and then compared to see the difference. 

# Unsecure Environment
<p align="center">
<img width="451" height="842" src="https://github.com/user-attachments/assets/3022dda8-dca0-4ccb-a17e-1f659a8679fd" />

# Secure Environment
<p align="center">
<img width="280" height="842" src="https://github.com/user-attachments/assets/c00899e3-0bc8-4b93-8b5e-d706e9c395b5" />


# Technology Utilized
- Azure Virtual Network
- Azure Network Security Group (NSG)
- Virtual Machine (Windows 10)
- Microsoft Sentinel (SIEM)
- Log Analytics Workspace for centralized log management
- Kusto Query Language (KQL)
- NIST SP 800-125B
- NIST SP 800-125

# Malicious Traffic Before
<img width="1962" height="1140" src="https://github.com/user-attachments/assets/5ca75af6-24a0-46a4-9e4e-d53ba7341be6" />
While in the insecure state, the VM logged 18387 failed login attempts in 24 hours. 
<img width="1952" height="1137" src="https://github.com/user-attachments/assets/fe61f728-4833-4da5-9fbd-6cf125314abe" />
The most common username used to attempt a login was administrator, being attempted 18107 times. 
<img width="1175" height="602" src="https://github.com/user-attachments/assets/09b3449f-bfe8-4082-8de3-ac7349b6f83e" />
The attack map reveals that most of the malicious traffic originated from Argentina.

# Malicious Traffic After
After implementing the secure environment and running the test for another 24 hours, 0 failed login attempts were logged, showing a 100% reduction in malicious traffic when compared to the unsecure environment.

# Conclusion

In this project, I set up a honeypot in Microsoft Azure, with central logs utilizing Log Analytics Workspace. Microsoft Sentinel was used to generate a map of where malicious traffic was originating from. This project shows the importance of properly securing network environments. By implementing security controls such as a zero-trust model and following recommendations from NIST SP 800-125B and NIST SP 800-125, malicious traffic was reduced by 100%, a massive improvement. 












---
