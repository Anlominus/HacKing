
  - [ ] 00 - Anonymity
  - [ ] 01 - Information Gathering
  - [ ] 02 - Vulnerability Assessment
  - [ ] 03 - Web Application HacKing
  - [ ] 04 - Database Assessment
  - [ ] 05 - Password HacKing
  - [ ] 06 - Wireless HacKing
  - [ ] 07 - Reverse Engineering
  - [ ] 08 - Exploit Frameworks & DataBases
  - [ ] 09 - Sniffing - Spoofing
  - [ ] 10 - Gaining & Maintaining Access
  - [ ] 11 - Digital Forensic
  - [ ] 12 - Analysis & Reporting
  - [ ] 13 - Social Engineering
  - [ ] 14 - Privilege Enumeration & Escalation
  - [ ] 15 - Malware Analysis Labs/Tools
  - [ ] 16 - Covering Tracks

---

- [ ] Anlominus:
  - [ ] 00 - Anonymity
    - [ ] 00 - Firewall Rules
      - [ ] [Iptables Essentials: Common Firewall Rules and Commands](https://github.com/trimstray/iptables-essentials)
    - [ ] 01 - Clear Logs
      - [ ] [Nullog](https://github.com/MrEmpy/Nullog)
    - [ ] 02 - Clear History
    - [ ] 03 - Change MAC Address
    - [ ] 04 - Change IP Address
    - [ ] 05 - Change Routing    
  - [ ] 01 - Information Gathering
    - [ ] 01 - Systems Information
      - [ ] [Th3inspector](https://github.com/Moham3dRiahi/Th3inspector)
      - [ ] [theHarvester](https://github.com/laramies/theHarvester)
      - [ ] [RED_HAWK](https://github.com/Tuhinshubhra/RED_HAWK)
    - [ ] 02 - Networks Information
      - [ ] [nmap](https://github.com/nmap/nmap)
    - [ ] 03 - Social Information
      - [ ] [sherlock](https://github.com/sherlock-project/sherlock)

    - [ ] 04 - SubDomain Information
      - [ ] [Anubis](https://github.com/jonluca/Anubis) 
  - [ ] 02 - Vulnerability Assessment
    - [ ] [PentMenu](https://github.com/GinjaChris/pentmenu)
    - [ ] [Legion](https://github.com/carlospolop/legion)
  - [ ] 03 - Web Application HacKing
    - [ ] [Hack-Tools](https://github.com/LasCC/Hack-Tools)
    - [ ] [BruteXSS](https://github.com/rajeshmajumdar/BruteXSS)
  - [ ] 04 - Database Assessment
  - [ ] 05 - Password HacKing
    - [ ] [JohnTheRipper](https://github.com/magnumripper/JohnTheRipper)
    - [ ] [hashcat](https://github.com/hashcat/hashcat)
    - [ ] [thc-hydra](https://github.com/vanhauser-thc/thc-hydra)

      - Hydra is a command line program brute forcer. The syntax is
        - `hydra -l <username> -P <path to wordlist> <IP> <service>`

      - If SSH is open for example, you can try
        - `hydra -l root -P <path to wordlist> <IP> ssh`

      Kali Linux comes with a 14 million password wordlist by default in /usr/share/wordlists/rockyou.txt.gz

      - You should extract this file.
        - `sudo gzip -d /usr/share/wordlists/rockyou.txt.gz`

      ### Some examples below, change the IP to your targets IP.

      - FTP:
        - `hydra -l admin -P /usr/share/wordlists/rockyou.txt 192.168.1.1 ftp -o ftp-result.txt`

      - TELNET:
        - `hydra -L /usr/share/wordlists/common-usernames -P /usr/share/wordlists/rockyou.txt 192.168.1.1 telnet`

      - SSH:
        - `hydra -l root -P /usr/share/wordlists/rockyou.txt 192.168.1.1 ssh -o ssh-result.txt`

      - Windows Remote Desktop
        - `hydra -t 1 -V -f -l administrator -P /usr/share/wordlists/rockyou.txt rdp://$ip`

      - Wordpress Admin login
        - `hydra -l admin -P ./passwordlist.txt $ip -V http-form-post '/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log In&testcookie=1:S=Location'`

      - SMB
        - `hydra -L usernames.txt -P passwords.txt $ip smb -V -f`

      - POP3
        - `hydra -l USERNAME -P /usr/share/wordlistsnmap.lst -f $ip pop3 -V`

      - SMTP
        - `hydra -P /usr/share/wordlistsnmap.lst $ip smtp -V  `

  - [ ] 06 - Wireless HacKing
    - [ ] [aircrack-ng](https://github.com/aircrack-ng/aircrack-ng)
    - [ ] [FruityWifi](https://github.com/xtr4nge/FruityWifi)
    - [ ] [bettercap](https://github.com/bettercap/bettercap)
    - [ ] [WiFi-Pumpkin](https://github.com/P0cL4bs/WiFi-Pumpkin)
    - [ ] [Wifipumpkin3](https://github.com/P0cL4bs/wifipumpkin3)
    - [ ] [Airgeddon](https://github.com/v1s1t0r1sh3r3/airgeddon)
    - [ ] [Airbash](https://github.com/tehw0lf/airbash)
    - [ ] [WireSpy](https://github.com/aress31/wirespy)
    - [ ] [aircrack-ng-gui](https://github.com/t-gitt/aircrack-ng-gui)
    - [ ] [Websploit](https://github.com/f4rih/websploit)
    - [ ] [LazyAircrack](https://github.com/3xploitGuy/lazyaircrack)
    - [ ] [SniffAir](https://github.com/Tylous/SniffAir)
    - [ ] [Kismet](https://github.com/kismetwireless/kismet)
    - [ ] [AirStrike](https://github.com/redcode-labs/AirStrike)
    - [ ] [Wireless IDS](https://github.com/SYWorks/wireless-ids/)
    - [ ] [Fern Wifi Cracker](https://github.com/savio-code/fern-wifi-cracker)
    - [ ] [OWT](https://github.com/clu3bot/OWT)
    - [ ] [getAir2U](https://github.com/v1s1t0r999/getAir2U)
    - [ ] [BeaconGraph](https://github.com/daddycocoaman/BeaconGraph)
    - [ ] [Wifi-Hacker](https://github.com/esc0rtd3w/wifi-hacker)
    - [ ] [Wifite2](https://github.com/derv82/wifite2)
    - [ ] [Infernal-Wireless v3](https://github.com/entropy1337/infernal-twin)
    - [ ] [BoopSuite](https://github.com/MisterBianco/BoopSuite)
    - [ ] [NetAttack2](https://github.com/chrizator/netattack2)
    - [ ] [HT-WPS-Breaker](https://github.com/SilentGhostX/HT-WPS-Breaker)
    - [ ] [KisMac2](https://github.com/IGRSoft/KisMac2)
  - [ ] 07 - Reverse Engineering
  - [ ] 08 - Exploit Frameworks & DataBases
    - [ ] [Metasploit Framework](https://github.com/rapid7/metasploit-framework)
    - [ ] [BeEF](https://github.com/beefproject/beef)
    - [ ] [The Social-Engineer Toolkit (SET)](https://github.com/trustedsec/social-engineer-toolkit)
    - [ ] [Bettercap](https://github.com/bettercap/bettercap)
    - [ ] [reNgine](https://github.com/yogeshojha/rengine)
    - [ ] [One-Lin3r](https://github.com/D4Vinci/One-Lin3r)
    - [ ] [MITMf](https://github.com/byt3bl33d3r/MITMf)
    - [ ] [TheFatRat](https://github.com/Screetsec/TheFatRat)
    - [ ] [LAZY](https://github.com/arismelachroinos/lscript)
    - [ ] [KitHack](https://github.com/AdrMXR/KitHack)
    - [ ] [PenBox](https://github.com/x3omdax/PenBox)
    - [ ] [PloitKit](https://github.com/rajeshmajumdar/PloitKit)
  - [ ] 09 - Sniffing - Spoofing
    - [ ] [ettercap](https://github.com/Ettercap/ettercap)
  - [ ] 10 - Gaining & Maintaining Access
  - [ ] 11 - Digital Forensic
  - [ ] 12 - Analysis & Reporting
  - [ ] 13 - Social Engineering
  - [ ] 14 - Privilege Enumeration & Escalation
    - [ ] Linux Enumeration:
      - [ ] [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings)
      - [ ] [PEASS-ng](https://github.com/carlospolop/PEASS-ng)
    - [ ]
  - [ ] 15 - Malware Analysis Labs/Tools
  - [ ] 16 - Covering Tracks
