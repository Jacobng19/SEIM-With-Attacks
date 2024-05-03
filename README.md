# SEIM Setup With Live Attacks

## Objective

To deploy Sentinel and integrate it with a VM acting as a honeypot, allowing real-time monitoring and analysis of cyber threats. Providing hands-on experience with setting up a SEIM, firewalls, brute force attacks, virtual machines, and more!

### Skills Learned

- SEIM Integration
- Querying Log Files
- Managing Network Inbound Rules
- Configuring Log Analytics
- Using Powershell Scripts
- Cyber Threat Monitoring
- Visualization Techniques
- Documenting & Reporting

### Tools Used

- Microsoft Azure
- Sentinel (SEIM)
- Log Analytics Workspace
- IP Geolocation API
- Powershell
- Windows Defender Firewall
  
## Project Steps

### Part 1: Creating Honeypot VM

![Screenshot 2024-04-24 213355](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/ffc4970b-e2de-44f3-8315-4349a1a65f3e)

*Ref 1: VM Creation

- My first step was creating a virtual machine within Azure that would sit out exposed on the internet to act as my honeypot, this virtual machine would be the foundation of the entire project so I wanted to create it first. Since I want threat actors to try to brute force the machine I made sure to have an extremely secure administrator password.

### Part 2: Opening Firewall

![Screenshot 2024-04-24 213154](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/f6bcd9ed-a078-49b6-864b-b41a6bbe91ef)

*Ref 2: VM Opening Ports

- My next step was opening the firewall from the Azure side. I started by opening all the ports in the inbound rules and also made sure to allow any protocol, all of this is an attempt to make the honeypot easy to find online when it is set live. While in the VM, I also turned off any additional Windows Dender Firewall protections too. This can be seen below in ref. image #3.

![Screenshot 2024-04-24 222218](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/8aeb6819-311a-4d20-8143-c2364b0421b4)

*Ref 3: VM Windows Defender Firewall

![Screenshot 2024-04-29 161212](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/ffc1f90e-c6c5-47dd-9479-52223f75a70b)

*Ref 4: Pinging Test

- To verify that the honeypot was now exposed, I took the public IP address that was provided by Azure and pinged the VM from my personal computer. It worked! So I knew the honeypot was in place.

### Part 3: Setting Up Log Analytics Workspace

![Screenshot 2024-04-24 213738](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/cdb9dea3-b4e6-4573-852c-1ba7b16758d1)

Ref 5: Workbook Creation

- The next order of action was to set up a Log Analytics workspace for a place to ingest the custom logs that I would need to pull from the VM. Once it was created, I connected the workspace to the honeypot VM. I also had to verify the data collection setting to make sure the workspace would be able to pull from the VM, which once turned on the workspace was ready to go!

### Part 4: Logging Into VM 

![Screenshot 2024-04-24 220020](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/9c441792-36dd-42e6-9d50-695c96e1b9de)
*Ref 6: Remote Accessing VM

![Screenshot 2024-04-24 222045](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/f754c358-1eff-4bfc-95e7-5ed6c57e8200)
*Ref 7: Windows Event Log Failure

### Part 5: Powershell Geodata Script

![Screenshot 2024-04-24 223719](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/0016f1ea-6370-46ac-923a-ac9f7b4520a2)
*Ref 8: Script Set-up

![Screenshot 2024-04-24 224313](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/d59c9d04-3b23-4cf6-828c-cd6e0437a747)
*Ref 9: Geodata Log File

### Part 6: Custom Log Creation

![Screenshot 2024-04-24 224643](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/3c370885-6223-4ab3-b356-4a10b16e3aac)
*Ref 10: Custom Log

### Part 7: Workbook & Map Visualization

![Screenshot 2024-04-29 143518](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/72e9448b-1635-4e1b-982a-e24dff2386a7)
*Ref 11: Workbook Creation


![Screenshot 2024-04-29 144838](https://github.com/Jacobng19/SEIM-With-Attacks/assets/167641578/25616134-46c3-40c8-8977-e08207d09a02)
*Ref 12: Final Attack Map


