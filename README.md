# Azure Honey Pot Project 

<img width="1477" height="805" alt="Azure Honey Pot Diagram drawio (2)" src="https://github.com/user-attachments/assets/0f70b68e-be4f-4c57-9b68-bb649b0fa4ee" />

The purpose of this project is to show the risk of having an insecure machine open to the internet and how a properly secured machine can greatly reduce the attack surface.

This project has two parts:

_**Unsecure Machine:**_ The Azure NSG firewall will be set to allow all traffic in, and the host-based firewall will be disabled. OS will be a barebones install with no updates.

_**Secure Machine:**_ As per the recommendations of NIST SP 800-125B, the Azure NSG firewall will be configured following a zero-trust model, only allowing connections from my IP. The host-based firewall will be enabled. Following the recommendations of NIST SP 800-125 for guest operating systems, the VM will be fully updated. 

# Technology Utilized


---
