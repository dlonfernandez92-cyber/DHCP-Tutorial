<h1>DHCP Tutorial</h1>

<h2>Description</h2>
This project is a tutorial that will walk you through setting up DHCP (Dynamic Host Configuration Protocol) services within your network. Once it's finished, we will connect a client to the network and confirm that it is receiving a new IP address from our DHCP services.
<br />

<h2>Environments Used </h2>

- <b>Windows Server 2016</b>
- <b>Windows 10</b>
- <b>Command Prompt</b>

<h2>Program walk-through:</h2>

<p align="center">
Launch Windows Server 2016, head to your server manager dashboard and select "add roles and features": <br/>
  <br/>
<img src="https://i.imgur.com/2khf4Ub.png" height="80%" width="80%" alt="DHCP Steps"/>
<br />
<br />
The wizard will begin. Click next and then select "Role Based or Feature Based Installation" :  <br/>
  <br/>
<img src="https://i.imgur.com/XVhUvY1.png" height="80%" width="80%" alt="DHCP Steps"/>
  <br/>
<img src="https://i.imgur.com/YjNwaOp.png" height="80%" width="80%" alt="DHCP Steps"/>  
<br />
<br />
Then you'll select your server and click next. You will then see a list of features and you'll want to select "DHCP Server" <br/>
  You'll then see a window showing the tools required for a DHCP server and you will select "Add Features": <br/>
  <br/>
<img src="https://i.imgur.com/jr62EMR.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
The next windows in the wizard will display the features added, notes about the DHCP Server and confirmation<br/>
that you want to install it. You will then be at the end of the wizard and you will now click install.  <br/>
<br/>
After it installs, you will then see another window saying that you'll need to "Complete DHCP configuration", you'll click it :  <br/>
<br/>
<img src="https://i.imgur.com/CyelPyK.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
The new window will have you review some delegations for the DHCP. After reviewing them, you will click commit<br/>
and close both the DHCP configuration window and the wizard window. You will have successfully created a DHCP server:  <br/>
<br/>
Now that you're back at the server manager dashboard, you'll click on tools and click "DHCP":  <br/>
<br/>
<img src="https://i.imgur.com/uNHb0FX.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br/>
<img src="https://i.imgur.com/szLHeD5.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
This brings us to the DHCP contols window. Here we will create a DHCP Scope. To do this, we will select our server and then<br/>
right click on "IPv4" and then click on "New Scope":  <br/>
<br/>
<img src="https://i.imgur.com/IwRjNGv.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
Once in the New Scope wizard, we will name our scope and then give it a range of IP addresses to use based on our network:  <br/>
<br/>
<img src="https://i.imgur.com/vPF5mGX.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
Next, we will list some exclusions. These are IP addresses that will be exluded and not used. Once added, click "add"<br/>
then click "next":  <br/>
<br/>
<img src="https://i.imgur.com/CxalgxA.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
You'll then determine the lease duration which is how long each client will utilize the IP address its assigned.<br/>
Then, you will be asked if you want to configure the DHCP, you will click yes. You'll then be shown a window to<br/>
assign a default gateway. This will be the IP address of your network. You'll type it in and click "add" then "next":  <br/>
<br/>
<img src="https://i.imgur.com/Dy86jLb.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
You will then choose to activate your scope and then click "finish". You'll then return to your DHCP controls window<br/>
and you will see your scope and that it is active:  <br/>
<br/>
<img src="https://i.imgur.com/I6K3bYQ.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
With our new DHCP scope active, we will head over to our client Windows 10 and check our current static IP address<br/>
by going to the command prompt and typing "ipconfig":  <br/>
<br/>
<img src="https://i.imgur.com/FGd4MmI.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
The current IP is static and without a default gateway. We will now use the next steps to have our client<br/>
request and receive a dynamic IP address from our DHCP server. In the command prompt, type "ncpa.cpl"<br/>
This command brings us to our network connections window and we can then right click on our connection<br/>
and click on "properties":  <br/>
<br/>
<img src="https://i.imgur.com/2ldeMqv.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
Within the properties window, you will then click on "Internet Protocol Version 4(TCP/IPv4)" and then click "properties":  <br/>
<br/>
<img src="https://i.imgur.com/CTw31NL.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
Within that properties window, you will select both "Obtain IP address automatically" and "Obtain DNS Server automatically"<br/>
and then click "ok":  <br/>
<br/>
<img src="https://i.imgur.com/pUbo6MZ.png" height="80%" width="80%" alt="DHCP Steps"/> 
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/jr62EMR.png" height="80%" width="80%" alt="DHCP Steps"/> 
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
