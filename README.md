# Azure-Enterprise-Network
Azure administration project demonstrating virtual networking, segmentation, secure VM administration, and monitoring.
## Project Overview
This project simulates an Azure enterprise environment designed to provide secure network segmentation, controlled administrative access, and centralized monitoring for cloud hosted resources. 

The environment uses a segmented Azure Virtual Network with dedicated subnets for management, application, and server workloads. Network Security Groups (NSGs) enforce least-privilege communication between subnets, while production servers remain private without directly assigned public IP addresses.

Azure Monitor Agent and Log Analytics provide centralized monitoring for the Windows Server environment. During implementation, a connectivity issue prevented the monitoring agent from retrieving its Data Collection Rule configuration. Troubleshooting identified that the server subnet was configured as a private subnet with no default outbound access. An Azure NAT Gateway was implemented to provide explicit outbound connectivity, allowing the agent to communicate with Azure Monitor while keeping the server private.

## Technologies Used

- Microsoft Azure
- Azure Virtual Network
- Network Security Groups (NSGs)
- Azure Virtual Machines
- Azure NAT Gateway
- Azure Monitor Agent
- Data Collection Rules
- Log Analytics Workspace
- Windows Server 2022
- IIS
- Ubuntu Linux
- PowerShell
