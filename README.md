# Cloud-Security-Sentinel-Lab

### Project Overview:
In this project I utilized a VM in Azure configured to be a honeypot, exposed to the internet to attract threat actors. The Powershell script included in this repository parses Windows Event Log information for failed RDP attacks and uses a third-party IP Geolocation API to collect geographic information about the attacker's location.
</b>
<br />
<br />
Azure Sentinel (SIEM) is connected to the live honeypot virtual machine. We will observe live attacks (RDP Brute Force) from all around the world. The custom PowerShell script provides the geolocation information allowing us to plot it on an Azure Sentinel Map.
</b>
<br />
<br />
<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon Windows Event Viewer and add Geolocation using an API

<h2>Other Tools</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API
- <b>Azure Sentinel:</b> Ingesting log information, mapping location information, and creating alerts
- <b>Azure VM:</b> Acted as a Honeypot to attackers across the globe allowing use to capture Brute Force RDP login attempts
- <b>Azure Log Analytics:</b> Took log information from a failed_rdp.log file created within the VM and created a custom MMA-based log where we were able to extract raw data 
