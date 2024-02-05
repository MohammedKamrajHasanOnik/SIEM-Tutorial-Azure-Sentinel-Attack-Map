<h1>SIEM-Tutorial-Azure-Sentinel-Attack-Map</h1>

<h2>(Anastasia Kuznetsova SIEM Tutorial Azure Sentinal Tutorial MAP with LIVE CYBER ATTACKS! followed)</h2>

<h2>Description</h2>
<b>This project is a guide of setting up Azure Sentinel, which is a cloud-based SIEM as well as Virtual Machine in the cloud, the VM will be our honeypot, will make it vulnerable to the internet, will monitor and log attacks from different IP addresses, different countries(was intended) however done local, afterwards will collect the data we will display it on a map, so we can see where all the attacks are coming.
<br/>

<h2>Languages and Utilities Used</h2>

- <b>Azure Sentinel</b> 
- <b>PowerShell Scripting and Transform Logs</b>
- <b>Azure Virtual Machine</b>
- <b>Log Analytics Workspace</b>
- <b>Remote Desktop Connection</b>
- <b>Kusto Query Language</b>
- <b>Azure log analytics workspace</b>
- <b>Azure Security Center</b>
- <b>Log Analytics Workspace</b>
- <b>Microsoft Defender Cloud</b>

<h2>Environments Used</h2>
- <b>Azure</b>
- <b>Windows 10 Virtual Machine</b>
- <b>Powershell ISE</b>



<h2>Links to programs and scripts required</h2>

- <b>Azure Portal:</b> https://portal.azure.com
- <b>API key ipgeolocation:</b> https://app.ipgeolocation.io/
- <b>Powerhsell Sentinel-Lab BRUTE_FORCE_ACTUAL.log (https://github.com/AnastasiaCoskuner/Sentinel-Lab/blob/main/BRUTE_FORCE_ACTUAL.log)
- <b>Query Log:</b>(https://github.com/AnastasiaCoskuner/Sentinel-Lab/blob/main/query_log)   

<h2 align="center">Program guide</h2>

<p align="center">
<b>The network diagram as shown I will be utilizing for the project</b> <br/>
<img src="https://i.imgur.com/HKW2M6b.jpeg"/>
<br />
<br />
<br />
<b>Creating virtual machine on azure basics filling out virtual machine name, image, user name, password, and selecting all inbound ports</b><br/> 
<img src="https://i.imgur.com/H5fQJrO.jpeg"/>
<br />
<br />
<br/>
<b>Creating Virutal machine disk size and os remains same no real reason to change<br/><br/>
<img src="https://i.imgur.com/YMlrCEu.jpeg"/>
<br />
<br />
<br/>
<b>Creating virtual machine networking need to select virtual network, subnet, NIC network security group must be advanced</b><br/> 
<img src="https://i.imgur.com/5Eevo5L.jpeg"/>
<br />
<br />
<br/>
<b>Deleting inbound rule 1000 and allowing ssh to allow as much ai or people to attack</b> <br/>
<img src="https://i.imgur.com/Yfp9XnK.jpeg"/>
<br />
<br />
<br/>
<b>Add inbound security to network security group virtual machine ports destination ports * means and all priority 100 is low also </b> <br/>
<img src="https://i.imgur.com/v80IQzL.jpeg"/>
<br />
<br />
<br/>
<b>Review creating a virtual machine whilst azure does operations in the background</b> <br/>
<img src="https://i.imgur.com/c0OGtDp.jpeg"/>
<br />
<br />
<br/>
<b>Deployed machine is complete virtual machine</b> <br/>
<img src="https://i.imgur.com/VfGl590.jpeg"/>
<br />
<br />
<br/>
<b>Searching Log analytics workspace for next step</b> <br/>
<img src="https://i.imgur.com/sJvUcCk.jpeg"/>
<br />
<br />
<br/>
<b>Creating log analytics workspace and resource group</b> <br/>
<img src="https://i.imgur.com/5vLONyj.jpeg"/>
<br />
<br />
<br/>
<b>Microsoft Azure log deployment analytics complete</b> <br/>
<img src="https://i.imgur.com/2J9NZio.jpeg"/>
<br />
<br />
<br/>
<b>Creating a new resource azure security center</b> <br/>
<img src="https://i.imgur.com/tkShJ27.jpeg"/>
<br />
<br />
<br/>
<b>Microsoft defender for cloud environment settings</b> <br/>
<img src="https://i.imgur.com/QSuR8d3.jpeg"/>
<br />
<br />
<br/>
<b>Put defender plan settings servers on sql server on machine off <br/>
<img src="https://i.imgur.com/6dhq38H.jpeg"/>
<br />
<br />
<br/>
<b>Settings for labtesthoneypot data collect changed to all events to allow virtual machine to collect data through powershell query and scripting coding <br/>
<img src="https://i.imgur.com/2r5c6ls.jpeg"/>
<br />
<br />
<br/>
<b>Next step is to manage settings labtesthoneypot to connect in log analytics workspace virtualmachine deprecated</b> <br/>
<img src="https://i.imgur.com/p9Fhaf1.jpeg"/>
<br />
<br />
<br/>
<b>Succesfully connected honeypot vm1</b> <br/>
<img src="https://i.imgur.com/eHgOESk.jpeg"/>
<br />
<br />
<br/>
<b>Creating Microsoft Sentinel </b> <br/>
<img src="https://i.imgur.com/hPvMxrO.jpeg"/>
<br />
<br />
<br/>
<b>Adding Azure sentinel labtesthoneypot</b> <br/>
<img src="https://i.imgur.com/30Iarwm.jpeg"/>
<br />
<br />
<br/>
<b>Azure sentinel free trial activated success</b> <br/>
<img src="https://i.imgur.com/B3Wc8gY.jpeg"/>
<br />
<br />
<br/>
<b>Got public IP Address of azure vm</b> <br/>
<img src="https://i.imgur.com/4fWccXO.jpeg"/>
<br />
<br />
<br/>
<b>Logged in remote desktop, event register security to check certain logins and details</b> <br/>
<img src="https://i.imgur.com/dO1rwwu.jpeg"/>
<br />
<br />
<br/>
<b>Domain profile off, private profile off public profile off in windows firewall</b> <br/>
<img src="https://i.imgur.com/CVCB0jy.jpeg"/>
<br />
<br />
<br/>
<b>Need api key from ipgeolocation to get traffic during vm sentinal attack</b> <br/>
<img src="https://i.imgur.com/5Ivm4j1.jpeg"/>
<br />
<br />
<br/>
<b>Powershell query changing api copying and pasting api from ipgeolocation</b> <br/>
<img src="https://i.imgur.com/LX7SPp1.jpeg"/>
<br />
<br />
<br/>
<b>An insinuation of what a local attack would look like on azure vm. Unfortunately could not do regional attack on azure vm. Due to coding changes, certain policies protocols, and certain changes not working as tried several sources. Poor lukegatesadmin :( </b> <br/>
<img src="https://i.imgur.com/EJ3ORAw.jpeg"/>
<br />
<br />
<br/>
<b>log analytics workspace labhoneypots tables create custom new MMA log</b> <br/>
<img src="https://i.imgur.com/7KSIwJ6.jpeg"/>
<br />
<br />
<br/>
<b>Creating custom log with path in tables</b> <br/>
<img src="https://i.imgur.com/PBAS8C6.jpeg"/>
<br />
<br />
<br/>
<b>Creating Microsoft sentinel map with the data first initial phase</b> <br/>
<img src="https://i.imgur.com/VH1finw.jpeg"/>
<br />
<br />
<br/>
<b>Running kusto query</b> <br/>
<img src="https://i.imgur.com/x7Cihnf.jpeg"/>
<br />
<br />
<br />
<b>Attack map this would have happened if reigional attack, if the powershell query and scripting worked and process.(Anastasia Kuznetsova SIEM Tutorial image used)</b> <br/>
<img src="https://i.imgur.com/6c9MEm5.jpeg"/>
<br />
<br />
<br/>
<br/>
<b>Force deleting all the resources to stop costs, very important if on pay as you go plan</b> <br/>
<img src="https://i.imgur.com/DFf8IgL.jpeg"/>
<br />
<br />
<br/>
