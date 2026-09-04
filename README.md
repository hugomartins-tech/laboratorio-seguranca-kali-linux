Laboratório de Segurança de Redes com Kali Linux

Sobre o projeto

Projeto acadêmico desenvolvido em ambiente virtualizado e controlado, com o objetivo de aplicar conhecimentos de Segurança da Informação e redes.
Durante o laboratório foram realizadas atividades de reconhecimento e varredura de rede, identificação de portas e serviços e testes de segurança utilizando ferramentas disponíveis no Kali Linux.

Ambiente

- Kali Linux
- CentOS
- VMware Workstation
- Rede TCP/IP

Ferramentas utilizadas

- Nmap
- Hydra
- Medusa

Atividades realizadas

- Reconhecimento do ambiente
- Varredura de rede
- Identificação de portas abertas
- Identificação de serviços
- Testes de segurança em ambiente autorizado
- Registro e documentação dos resultados

Resultados

Os resultados obtidos durante as atividades foram registrados e analisados conforme os requisitos do projeto acadêmico.

Observação

Todos os testes foram realizados em ambiente virtualizado, controlado e autorizado, exclusivamente para fins acadêmicos.

Varredura 

Starting Nmap 7.70 ( https://nmap.org ) at 2026-03-22 17:43 -03
NSE: Loaded 148 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 17:43
Completed NSE at 17:43, 0.00s elapsed
Initiating NSE at 17:43
Completed NSE at 17:43, 0.00s elapsed
Initiating ARP Ping Scan at 17:43
Scanning 192.168.136.130 [1 port]
Completed ARP Ping Scan at 17:43, 0.00s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 17:43
Completed Parallel DNS resolution of 1 host. at 17:43, 0.02s elapsed
Initiating SYN Stealth Scan at 17:43
Scanning 192.168.136.130 [1000 ports]
Discovered open port 111/tcp on 192.168.136.130
Discovered open port 80/tcp on 192.168.136.130
Discovered open port 22/tcp on 192.168.136.130
Discovered open port 21/tcp on 192.168.136.130
Completed SYN Stealth Scan at 17:43, 0.07s elapsed (1000 total ports)
Initiating Service scan at 17:43
Scanning 4 services on 192.168.136.130
Completed Service scan at 17:43, 6.14s elapsed (4 services on 1 host)
Initiating OS detection (try #1) against 192.168.136.130
NSE: Script scanning 192.168.136.130.
Initiating NSE at 17:43
NSE: [ftp-bounce] PORT response: 500 Illegal PORT command.
Completed NSE at 17:43, 0.68s elapsed
Initiating NSE at 17:43
Completed NSE at 17:43, 0.01s elapsed
Nmap scan report for 192.168.136.130
Host is up (0.00061s latency).
Not shown: 996 closed ports
PORT    STATE SERVICE VERSION
21/tcp  open  ftp     vsftpd 3.0.2
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_drwxr-xr-x    2 0        0               6 Jun 09  2021 pub
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to ::ffff:192.168.136.128
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 1
|      vsFTPd 3.0.2 - secure, fast, stable
|_End of status
22/tcp  open  ssh     OpenSSH 7.4 (protocol 2.0)
| ssh-hostkey: 
|   2048 78:3f:f6:97:af:0a:6e:3f:85:d1:e4:82:a9:b9:a4:f7 (RSA)
|   256 7e:4d:42:0c:7e:79:f8:3d:f0:c6:15:f7:30:d3:00:da (ECDSA)
|_  256 9b:1f:2b:55:e0:64:86:1c:46:ad:ea:dd:67:00:20:e8 (ED25519)
80/tcp  open  http    Apache httpd 2.4.6 ((CentOS))
| http-methods: 
|   Supported Methods: POST OPTIONS GET HEAD TRACE
|_  Potentially risky methods: TRACE
|_http-server-header: Apache/2.4.6 (CentOS)
|_http-title: Apache HTTP Server Test Page powered by CentOS
111/tcp open  rpcbind 2-4 (RPC #100000)
| rpcinfo: 
|   program version   port/proto  service
|   100000  2,3,4        111/tcp  rpcbind
|_  100000  2,3,4        111/udp  rpcbind
MAC Address: 00:0C:29:A4:BE:4D (VMware)
Device type: general purpose
Running: Linux 3.X|4.X
OS CPE: cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:4
OS details: Linux 3.2 - 4.9
Uptime guess: 0.017 days (since Sun Mar 22 17:18:26 2026)
Network Distance: 1 hop
TCP Sequence Prediction: Difficulty=253 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Unix

TRACEROUTE
HOP RTT     ADDRESS
1   0.61 ms 192.168.136.130

NSE: Script Post-scanning.
Initiating NSE at 17:43
Completed NSE at 17:43, 0.00s elapsed
Initiating NSE at 17:43
Completed NSE at 17:43, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 10.48 seconds
           Raw packets sent: 1023 (45.806KB) | Rcvd: 1015 (41.294KB)

