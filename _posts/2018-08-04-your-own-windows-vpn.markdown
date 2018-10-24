---
layout: post
title:  "Your own Windows VPN to use anywhere"
date:   2018-08-04 06:00:11 +0300
categories: windows
tags:
- windows
- vpn
- proxy
- nat
- internet
---
Consider this, you're in a dystopian universe with a Windows server hosted on EvilCorp™ datacenters.

You cancel your $19.99 / month VPN subscription at the hopes of replacing it with your Window server.

Here are the steps:

1. Open 'Add Roles & Features'.
2. Add 'Remote Access'.
3. Open 'Routing and Remote Access'.
4. Right-click on your server name and click 'Configure and Enable Routing and Remote Access'.
5. Choose Custom.
6. Select 'VPN' and 'NAT'.
7. Navigate to IPv4 -> NAT.
8. 'New Interface'.
9. Add 'Internal'. ('Private interact connected to private network' will be checked)
10. Add 'Ethernet' (or the name of the adapter with internet)
	- Make sure 'Public interface connecte to the Internet' is checked.
	- Make sure 'Enable NAT on this interface' is checked.
11. On the server name, right click and click 'Properties'.
12. Make sure under 'IPv4 Router' you have 'LAN and demand-dial routing' is checked.
13. In the IPv4 tab, select 'Static address pool'.
14. Assign some IP address. (I chose 192.168.40.10 -> 192.168.40.20)
15. Save and close!

Now, on your client machine, you can create a new VPN and you will be able to successfully
browse the internet using your dedicated Windows server's IP address.
