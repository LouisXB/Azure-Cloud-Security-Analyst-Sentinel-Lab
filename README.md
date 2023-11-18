# Cloud-Security-Sentinel-Lab

### Project Overview:
In this project I utilized a honey VM in Azure, exposed to the internet to attract threat actors. The Powershell script included in this repository parses Windows Event Log information for failed RDP attacks and uses a third-party IP Geolocation API to collect geographic information about the attacker's location.

For a more depth step by step blog, visit: https://github.com/LouisXB/LouisXB.github.io/blob/main/_posts/2023-11-17-cloud-security-analyst.md
</b>
<br />
<br />
Azure Sentinel (SIEM) is connected to the live honeypot virtual machine. This allows us to observe live attacks (RDP Brute Force) from all around the world. The custom PowerShell script provides the geolocation information allowing us to plot it on an Azure Sentinel Map.
</b>
<br />
<br />
<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon Windows Event Viewer and add Geolocation using an API

### Running the Custom Powershell log in the Virtual Machine
![custom_log](https://github.com/LouisXB/Cloud-Security-Sentinel-Lab/assets/115196076/404879d9-f678-4b26-96bf-dd2bf486bdc0)
*Attacks incoming from Singapore


<h2>Other Tools</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API
![ipgeolocation_api](https://github.com/LouisXB/Cloud-Security-Sentinel-Lab/assets/115196076/3d2773a8-1d3e-48d1-b11f-4adf0081b15e)

- <b>Azure Sentinel:</b> Ingesting log information, mapping location information, and creating alerts
![sentinel mapping](https://github.com/LouisXB/Cloud-Security-Sentinel-Lab/assets/115196076/3729b777-0196-43fc-97ab-337c896488d0)
Map shows 88 attacks in Singapore within 3 minutes of running

- <b>Azure VM:</b> Acted as a Honeypot to attackers across the globe allowing use to capture Brute Force RDP login attempts
- <b>Azure Log Analytics:</b> Took log information from a failed_rdp.log file created within the VM and created a custom MMA-based log where we were able to extract raw data 



