<h1>SIEM-Tutorial-Azure-Sentinel-Attack-Map</h1>

<h2>(Anastasia Kuznetsova SIEM Tutorial Azure Sentinal Tutorial MAP with LIVE CYBER ATTACKS! followed)</h2>

<h2>Description</h2>
<b>This project is a guide of setting up Azure Sentinel, which is a cloud-based SIEM as well as Virtual Machine in the cloud, the VM will be our honeypot, will make it vulnerable to the internet, will monitor and log attacks from different IP addresses, different countries, afterwards will collect the data we will display it on a map, so we can see where all the attacks are coming.
<br/>

<h2>Languages and Utilities Used</h2>

- <b>Azure Sentinel</b> 
- <b>PowerShell Scripting and Transform Logs</b>
- <b>Azure Virtual Machine</b>
- <b>Log Analytics Workspace</b>
- <b>Remote Desktop Connection</b>


<h2>Environments Used</h2>
- <b>Azure</b>
- <b>Windows 11 Azure Virtual machine</b>
- <b>Powershell ise x86</b>

<h2>Links to programs and scripts required</h2>

- <b>Azure Portal:</b> https://portal.azure.com
- <b>API key ipgeolocation:</b> https://app.ipgeolocation.io/
- <b>Powerhsell Sentinel-Lab BRUTE_FORCE_ACTUAL.log (https://github.com/AnastasiaCoskuner/Sentinel-Lab/blob/main/BRUTE_FORCE_ACTUAL.log)


<h2 align="center">Program guide</h2>

<p align="center">
<b>The network diagram as shown I will be utilizing for the project</b> <br/>
<img src="https://i.imgur.com/HKW2M6b.jpeg"/>
<br />
<br />
<br />
<b>Creating Server 2019, assigning it 2048mb memory ram approx 2gb and 3 processors VM</b> <br/>
<img src="https://i.imgur.com/nqjMOCy.jpg"/>
<br />
<br />
<br/>
