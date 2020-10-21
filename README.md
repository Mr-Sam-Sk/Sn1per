# Sn1per
From a new Docker console, run the following commands.  
Download https://raw.githubusercontent.com/1N3/Sn1per/master/Dockerfile 
docker build -t sn1per .  
docker run -it sn1per /bin/bash  
or   
docker pull xerosecurity/sn1per docker run -it xerosecurity/sn1per /bin/bash 


USAGE: 
[*] NORMAL MODE sniper -t &lt;TARGET>  
[*] NORMAL MODE + OSINT + RECON sniper -t &lt;TARGET> -o -re  
[*] STEALTH MODE + OSINT + RECON sniper -t &lt;TARGET> -m stealth -o -re  
[*] DISCOVER MODE sniper -t &lt;CIDR> -m discover -w &lt;WORSPACE_ALIAS>  
[*] SCAN ONLY SPECIFIC PORT sniper -t &lt;TARGET> -m port -p &lt;portnum>  
[*] FULLPORTONLY SCAN MODE sniper -t &lt;TARGET> -fp  
[*] WEB MODE - PORT 80 + 443 ONLY! sniper -t &lt;TARGET> -m web  
[*] HTTP WEB PORT MODE sniper -t &lt;TARGET> -m webporthttp -p &lt;port>  
[*] HTTPS WEB PORT MODE sniper -t &lt;TARGET> -m webporthttps -p &lt;port>  
[*] HTTP WEBSCAN MODE sniper -t &lt;TARGET> -m webscan   
[*] ENABLE BRUTEFORCE sniper -t &lt;TARGET> -b  
[*] AIRSTRIKE MODE sniper -f targets.txt -m airstrike  
[*] NUKE MODE WITH TARGET LIST, BRUTEFORCE ENABLED, FULLPORTSCAN ENABLED, OSINT ENABLED, RECON ENABLED, WORKSPACE &amp; LOOT ENABLED sniper -f targets.txt -m nuke -w &lt;WORKSPACE_ALIAS>  
[*] MASS PORT SCAN MODE sniper -f targets.txt -m massportscan  
[*] MASS WEB SCAN MODE sniper -f targets.txt -m massweb  
[*] MASS WEBSCAN SCAN MODE sniper -f targets.txt -m masswebscan  
[*] MASS VULN SCAN MODE sniper -f targets.txt -m massvulnscan  
[*] PORT SCAN MODE sniper -t &lt;TARGET> -m port -p &lt;PORT_NUM>  
[*] LIST WORKSPACES sniper --list  
[*] DELETE WORKSPACE sniper -w &lt;WORKSPACE_ALIAS> -d  
[*] DELETE HOST FROM WORKSPACE sniper -w &lt;WORKSPACE_ALIAS> -t &lt;TARGET> -dh  
[*] GET SNIPER SCAN STATUS sniper --status  
[*] LOOT REIMPORT FUNCTION sniper -w &lt;WORKSPACE_ALIAS> --reimport  
[*] LOOT REIMPORTALL FUNCTION sniper -w &lt;WORKSPACE_ALIAS> --reimportall  
[*] LOOT REIMPORT FUNCTION sniper -w &lt;WORKSPACE_ALIAS> --reload  
[*] LOOT EXPORT FUNCTION sniper -w &lt;WORKSPACE_ALIAS> --export  
[*] SCHEDULED SCANS sniper -w &lt;WORKSPACE_ALIAS> -s daily|weekly|monthly  
[*] USE A CUSTOM CONFIG sniper -c /path/to/sniper.conf -t &lt;TARGET> -w &lt;WORKSPACE_ALIAS>  
[*] UPDATE SNIPER sniper -u|--update MODES: NORMAL: Performs basic scan of targets and open ports using both active and passive checks for optimal performance. STEALTH: Quickly enumerate single targets using mostly non-intrusive scans to avoid WAF/IPS blocking. FLYOVER: Fast multi-threaded high level scans of multiple targets (useful for collecting high level data on many hosts quickly). AIRSTRIKE: Quickly enumerates open ports/services on multiple hosts and performs basic fingerprinting. To use, specify the full location of the file which contains all hosts, IPs that need to be scanned and run ./sn1per /full/path/to/targets.txt airstrike to begin scanning. NUKE: Launch full audit of multiple hosts specified in text file of choice. Usage example: ./sniper /pentest/loot/targets.txt nuke. DISCOVER: Parses all hosts on a subnet/CIDR (ie. 192.168.0.0/16) and initiates a sniper scan against each host. Useful for internal network scans. PORT: Scans a specific port for vulnerabilities. Reporting is not currently available in this mode. FULLPORTONLY: Performs a full detailed port scan and saves results to XML. MASSPORTSCAN: Runs a "fullportonly" scan on mutiple targets specified via the "-f" switch. WEB: Adds full automatic web application scans to the results (port 80/tcp &amp; 443/tcp only). Ideal for web applications but may increase scan time significantly. MASSWEB: Runs "web" mode scans on multiple targets specified via the "-f" switch. WEBPORTHTTP: Launches a full HTTP web application scan against a specific host and port. WEBPORTHTTPS: Launches a full HTTPS web application scan against a specific host and port. WEBSCAN: Launches a full HTTP &amp; HTTPS web application scan against via Burpsuite and Arachni. MASSWEBSCAN: Runs "webscan" mode scans of multiple targets specified via the "-f" switch. VULNSCAN: Launches a OpenVAS vulnerability scan. MASSVULNSCAN: Launches a "vulnscan" mode scans on multiple targets specified via the "-f" switch.
