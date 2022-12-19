# PiHoleInsigniaDNS

Add the Insignia DNS records to your local PiHole which allows you to use Automatic IP and DNS setting in your XBOX.

Installation and setup of PiHole is beyond the scope of this document and is very well documented at the pi-hole.net website.

Background:
Upon the launch of Insignia the support forums have been virtually flooded with DNS related issues with various resolutions where most of the issues are DNS (Dynamic Name Resolution) related.  DNS is a fundamental element of how the internet works and is basically how computers find each each other.
The original XBOX Live system has a few "baked in" DNS records that need to be re-directed to the Insignia servers in order for your XBOX to work with the Insignia service.

There are many ways to resolve this issue and this is simply another one that is easy to impliment if you already have PiHole in your network.

From the PiHole Admin Panel > Local DNS > DNS Records

![image](https://user-images.githubusercontent.com/4142046/208539253-4a172d97-21a1-445a-88c4-3610b387733f.png)

Add the 3 domains (as.xboxlive.com, macs.xboxlive.com, tgs.xboxlive.com) and 1 IP Address (46.101.64.175) and click the Add button.

![image](https://user-images.githubusercontent.com/4142046/208539758-dccfb89f-c287-4e12-94de-c568b9f7fde0.png)

When the screen refreshes you should have 3 new DNS entries.

![image](https://user-images.githubusercontent.com/4142046/208539958-6a389e83-2dba-4911-8e3a-ef1347ab04b4.png)

If your XBOX is already configured for Automatic it may be able to connect to the Insignia service after a restart or reboot.

Below is for reference.

Your Router should already be configured to use your PiHole as part of the PiHole setup which is beyond the scope of this document.
Here is my configuration as an example.  Your settings will be different!

![image](https://user-images.githubusercontent.com/4142046/208540724-0bdcf1b1-ac8c-4a10-9c72-e624109bc5b2.png)

XBOX Settings:
Xbox Admin > System > Settings > Network Settings (Example)

![image](https://user-images.githubusercontent.com/4142046/208548184-e69d3523-a203-4f23-be74-aa2cb7a519b6.png)

Note the current IP Address is at the top.
When set to DHCP the IP Address, Subnet Mask and Gateway IP are not relevant.

In your MS Dashboard your Network Settings should be set for Automatic.

![image](https://user-images.githubusercontent.com/4142046/208547945-239c75f8-3082-49ff-8b72-0fcd5903f4f6.png)

Including your DNS Settings.

![image](https://user-images.githubusercontent.com/4142046/208548002-b9bed32c-9cd1-42c9-a524-5d8669d04266.png)

