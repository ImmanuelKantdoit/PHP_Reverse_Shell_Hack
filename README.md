# PenTesting
Gameplan for doing PenTesting

- DIscover your IP Address
- Discover Target Machine's IP.
- Discover Open Ports using NMAP or RUSTSCAN
- If a website, enumerate using Nikto or Dirb
    - Check for /robots.txt
    - Check for login pages
    - Check for Vulnerabilities using Searchsploit
- Based on recon, determine or try these approaches:
    - Brute forcing
    - Remote Code Execution
          - Check if the machine's website is vulnerable to this
          - If so, check the level of access, if not root, proceed to reverse shell hack
    - Reverse Shell Hack
          - Use reverse shell generator online, generate a reverse shell code here or find a reverse shell code/cheat code
          - Download the file in the target's machine
          - Open listner, using NetCat
          - start a python server on your machine
          - Download the file on the target machine using wget
          - Open the file
      - Shells would usually be unstable
          - To make it stable use: python3 -c 'import pty; pty.spawn ("/bin/bash")'
          - Then use: export TERM=xterm
          - Then use: CTRL + Z
          - Then use: stty raw -echo; fg
