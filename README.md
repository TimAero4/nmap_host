# nmap_host
#<ins>Сканирование хоста</ins>
## 1.Vulnerabilities
1. [nmap_sV](image/nmap_sV.png)
2. [openssh](image/OpenSSH.png)
3. [vsftpd](image/vsftpd.png)
### Links_with_vuln
4. [openssh_1](https://www.exploit-db.com/exploits/45233)
5. [openssh_2](https://www.exploit-db.com/exploits/45210)
6. [openssh_3](https://www.exploit-db.com/exploits/40963)
7. [vsftpd_1](https://www.exploit-db.com/exploits/17491)
8. [vsftpd_2](https://www.exploit-db.com/exploits/49757)
## 2.Nmap_scan
1. [nmap_SYN](image/nmap_sS.png)
### SYN-scan Это полуоткрытое сканирование. Полное трехэтапное сканирование не инициализируется. 
### Сканер отправляет пакет с SYN флагом, в ответ SYN/ACK, далее в ответ вместо ACK идёт отправка RST.
2. [nmap_sF](image/nmap_sF.png)
### FIN-scan Сканер отправляет пакет с флагом FIN(соединение уже установленно).
### Сервер не ожидает получить такой флаг на закрытый порт. На данном ответе и построена логика понимания открыт ли порт.
3. [nmap_sX](image/nmap_sX.png)
### Xmas-scan Сканер отправляет сразу пакет с несколькими флагами FIN PSH URG.
### Данное сканирование способно обойти некоторые типы файерволлов. Логика работы
### похожа на FIN, разница в наборе бит, отправляемых в пакете.
4. [nmap_sU](image/nmap_sU.png)
### UDP-scan Сканер отправляет пустой пакет на порт
### UDP не использует рукопожатие и флагов. На закрытом порту сервер отвечает ICMP пакетом (Port Unreachable).
### Если ответа нету-порт открыт либо отфильтрован файерволлом.

