# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## PROGRAM:
**CLIENT**
```
client.py
import socket
from pythonping import ping
s=socket.socket() s.bind(('localhost'8000)) s.listen(5) c,addr=s.accept()
while True: hostname=c.recv(1024).decode() try:
c.send(str(ping(hostname, verbose=False)).encode())
except KeyError:
c.send("Not Found".encode())
```
**SERVER**
```
server.py

import socket s=socket.socket() s.connect(('localhost',8000)) while True:
ip=input("Enter the website you want to ping ")
s.send(ip.encode())
print(s.recv(1024).decode())
```
## Output
**NESTAT:**
<img width="700" height="458" alt="image" src="https://github.com/user-attachments/assets/b4d0e964-25d6-4750-b4d7-7e27c0836dbd" />

**IP CONFIGURATION:**
<img width="639" height="486" alt="image" src="https://github.com/user-attachments/assets/04e73944-0856-4697-b6bd-5cc61d2be84e" />

**GETMAC:**
<img width="794" height="177" alt="image" src="https://github.com/user-attachments/assets/191b4ce7-0e82-484b-90d3-7deae617d99b" />

**ARP:**
<img width="822" height="508" alt="image" src="https://github.com/user-attachments/assets/927ee8fe-0bc3-488f-a866-df68af85fa32" />

**SYSTEM INFO:**
<img width="776" height="600" alt="image" src="https://github.com/user-attachments/assets/e78f4dcf-56e4-461b-9d6b-3e5d0bd050b3" />

**NBTSTAT:**
<img width="790" height="383" alt="image" src="https://github.com/user-attachments/assets/a33528df-916f-4967-bba5-41ea10b9d958" />

**HOST NAME:**
<img width="768" height="245" alt="image" src="https://github.com/user-attachments/assets/456b6b6c-06e6-4f9f-b179-197188b3386f" />

**NS LOOKUP:**
<img width="783" height="177" alt="image" src="https://github.com/user-attachments/assets/fd9ba1cf-feb4-4f09-a63c-95beaacc93a3" />

**PING:**
<img width="796" height="575" alt="image" src="https://github.com/user-attachments/assets/aa127fb9-8dae-4695-822f-ecfcd167e38a" />

**TRACET:**
<img width="805" height="105" alt="image" src="https://github.com/user-attachments/assets/63575ec0-93f6-4f03-9843-6a3d1504ec11" />

## Result
Thus Execution of Network commands Performed 
