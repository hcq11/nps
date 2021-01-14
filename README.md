
# NPS
![](https://img.shields.io/github/stars/ehang-io/nps.svg)   ![](https://img.shields.io/github/forks/ehang-io/nps.svg)
[![Gitter](https://badges.gitter.im/cnlh-nps/community.svg)](https://gitter.im/cnlh-nps/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
![Release](https://github.com/ehang-io/nps/workflows/Release/badge.svg)
![GitHub All Releases](https://img.shields.io/github/downloads/ehang-io/nps/total)

[README](https://github.com/ehang-io/nps/blob/master/README.md)|[中文文档](https://github.com/ehang-io/nps/blob/master/README_zh.md)

NPS is a lightweight, high-performance, powerful **intranet penetration** proxy server, with a powerful web management terminal.


![image](https://github.com/ehang-io/nps/blob/master/image/web.png?raw=false)

## Feature

- Comprehensive protocol support, compatible with almost all commonly used protocols, such as tcp, udp, http(s), socks5, p2p, http proxy ...
- Full platform compatibility (linux, windows, macos, Synology, etc.), support installation as a system service simply.
- Comprehensive control, both client and server control are allowed.
- Https integration, support to convert backend proxy and web services to https, and support multiple certificates.
- Just simple configuration on web ui can complete most requirements.
- Complete information display, such as traffic, system information, real-time bandwidth, client version, etc.
- Powerful extension functions, everything is available (cache, compression, encryption, traffic limit, bandwidth limit, port reuse, etc.)
- Domain name resolution has functions such as custom headers, 404 page configuration, host modification, site protection, URL routing, and pan-resolution.
- Multi-user and user registration support on server.

**Didn't find the feature you want? It doesn't matter, click [Enter the document](https://ehang-io.github.io/nps/) to find it!**

## Quick start

### Installation && Run

- server  
docker run -d --name nps --net=host hcq11/nps-server:latest

- client    
docker run -d --name npc -e NPC_SERVER_ADDR=127.0.0.1:8024 -e NPC_SERVER_VKEY=123fdafa -e TYPE=tcp hcq11/npc-cli:latest

### note:
- Replace NPC_SERVER_ADDR ip:port with NPS ServerIP:port,the default port is 8024.  
- Replace NPC_SERVER_VKEY with web management from client startup command.

### default ports

The default configuration file of nps use 80，443，8080，8024 ports

80 and 443 ports for host mode default ports

8080 for web management access port

8024 for net bridge port, to communicate between server and client

- Access server IP:web service port (default is 8080).
- Login with username and password (default is admin/123, must be modified when officially used).
- Create a client.

### Client connection
- Click the + sign in front of the client in web management and copy the startup command.
- Execute the startup command, Linux can be executed directly, Windows will replace ./npc with npc.exe and execute it with cmd.

### Configuration
- After the client connects, configure the corresponding penetration service in the web.
- For more advanced usage, see [Complete Documentation](https://ehang-io.github.io/nps/)

## Contribution
- If you encounter a bug, you can submit it to the dev branch directly.
- If you encounter a problem, you can feedback through the issue.
- The project is under development, and there is still a lot of room for improvement. If you can contribute code, please submit PR to the dev branch.
- If there is feedback on new features, you can feedback via issues or qq group.
