# Masscan_to_Nmap
Python script that runs Masscan against an IP to collect open ports, feed those ports to Nmap, which finds service versions and runs default scripts. Built with CTFs in mind.

## Description

My main process for CTFs was to run Masscan, which would find the TCP & UDP ports that were open on a target. I'd then copy and paste those open ports, and ask Nmap to run those ports and find the service versions and run the default enumeration scripts.

I wanted to automate this, so I could just fire off a script with a given IP and then go and make a coffee whilst it runs. This script prints out the Nmap results and also saves a copy in your directory as well.

### Installation
```bash
wget https://raw.githubusercontent.com/hack-parthsharma/Masscan-to-Nmap/main/masscan_to_nmap.py
```
### Usage
```bash
sudo python3 masscan_to_nmap.py -i 10.10.10.11
```
Adding the `-n` flag will specify the network, such as eth0 or tun0. If you don't specify a network flag, it will take tun0 as the default network to use. 

![options](https://github.com/hack-parthsharma/Masscan-to-Nmap/blob/main/images/Options.png)

### Examples
![Masscan_Nmap](https://github.com/hack-parthsharma/Masscan-to-Nmap/blob/main/images/masscan_nmap.png)

### Known Issues

Masscan can hang and start counting into the minus numbers. It normally resolves itself under 'minus' 200 seconds, if not sooner. It's a masscan issue, related to scanning when using a VPN. 

### Contact
If you notice a way the script can be improved you're welcome to make requests and raise issues. 

#### License
This tool is free to use. Do not use for illegal purposes. Only use for academic purposes, on computers that you have permission to access. 
