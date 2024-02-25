<h1>Active Directory Domain Lab</h1>

<h2>Description</h2>
The primary objectives of this lab are to install and configure Active Directory Domain Services onto a domain controller, create an admin user account, join users to the domain using a Powershell script, and connect a test-client to the domain.  The DC will also function as the DHCP, DNS, and Remote Access server for the test network.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Oracle VirtualBox</b>
- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10 Pro</b>

<h2>Project walk-through:</h2>

<p align="center">
Launch Server Manager and select <b>Add roles and features</b>: <br/>
<img src="https://i.imgur.com/hZttzCq.png" height="80%" width="80%"/>
<br />
<br />
Once AD is installed, run the configuration wizard to create a new forest:  <br/>
<img src="https://i.imgur.com/FUfQVg6.png" height="80%" width="80%"/>
<br />  
<br />
Create a new Organizational Unit named _ADMINS and add a new user: <br/>
<img src="https://i.imgur.com/wZXWx8v.png" height="80%" width="80%" />
<br />
<br />
Under the new user's properties settings, add the user to the Domain Admins group:  <br/>
<img src="https://i.imgur.com/9GlPSFz.png" height="80%" width="80%" />
<br />
<br />
Install the Routing and Remote Access server role with NAT so clients can reach the internet:  <br/>
<img src="https://i.imgur.com/iWZUtk7.png" height="80%" width="80%" />
<br />
<br />
Install the DHCP server role and add a new scope for the LAN clients:  <br/>
<img src="https://i.imgur.com/Ld0TrX7.png" height="80%" width="80%" />
<br />
<br />
After creating the _USERS organizational unit in Active Directory, this script will add a predefined list of user accounts:  <br/>
<img src="https://i.imgur.com/dPgMaJx.png" height="80%" width="80%" />
<br />
<br />
Run the script:  <br/>
<img src="https://i.imgur.com/PVKFXuN.png" height="80%" width="80%" />
<br />
<br />
Confirm the script executed successfully:  <br />
<img src="https://i.imgur.com/qMUspNT.png" height="80%" width="80%" />
<br />
<br />
Over on the Windows 10 VM it's time to join the domain:  <br />
<img src="https://i.imgur.com/DCh2rJr.png" height="80%" width="80%" />
<br />
<br />
Finally, log back into Windows 10 using one of the users created previously and test connectivity:  <br />
<img src="https://i.imgur.com/SfT47I4.png" height="80%" width="80%" />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
