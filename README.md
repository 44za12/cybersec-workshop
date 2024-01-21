# IIT Delhi Ethical Hacking 20th - 21st January

## Topics Covered:
- OWASP TOP 10

- Information Gathering
    - Service Discovery
    - Subdomain Enumeration
    - Directory Enumeration
    - OSINT
    - Email Harvesting
    - Social Engineering

- Tools covered:
    - subfinder:
        - Homepage: https://github.com/projectdiscovery/subfinder
        - Installation: `go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest`
        - Example: `subfinder -d <target.com>`

    - rustscan:
        - Homepage: https://github.com/RustScan/RustScan
        - Installation: `alias rustscan='docker run -it --rm --name rustscan rustscan/rustscan:2.1.1'`
        - Example: `rustscan -a <targetip> —ulimit 10000 — -A`

    - whois:
        - Homepage: https://github.com/sheepla/whois-cli
        - Installation: `go install github.com/sheepla/whois-cli@latest`
        - Example: `whois <targetip>`

    - theHarvester:
        - Homepage: https://github.com/sheepla/whois-cli
        - Installation: https://github.com/laramies/theHarvester/wiki/Installation
        - Example: `theHarvester -d target.com -l 500 -b duckduckgo`

    - gobuster:
        - Homepage: https://github.com/OJ/gobuster
        - Installation: `go install github.com/OJ/gobuster/v3@latest`
        - Example: `gobuster dir -u target.com -w dirlist.txt`

    - gobuster:
        - Homepage: https://github.com/Mebus/cupp
        - Installation: `git clone https://github.com/Mebus/cupp.git`
        - Example: `python3 cupp.py`

    - cewl:
        - Homepage: https://github.com/digininja/CeWL
        - Installation: https://github.com/digininja/CeWL
        - Example: `cewl`

    - hydra:
        - Homepage: https://github.com/vanhauser-thc/thc-hydra
        - Installation: `sudo apt-get install hydra`
        - Example: `hydra -L users.txt -P rockyou_7k.txt 'http-get-form://127.0.0.1:8080/vulnerabilities/brute/:username=^USER^&password=^PASS^&Login=Login:H=Cookie\:PHPSESSID={SESSION_ID}; security=low:F=Username and/or password incorrect'`
        
    - sqlmap:
        - Homepage: https://github.com/sqlmapproject/sqlmap
        - Installation: `pip3 install sqlmap`
        - Example: `sqlmap -r request.txt -D dvwa -T users -C user,password --dump`

