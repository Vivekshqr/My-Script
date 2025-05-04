SafeSquid Proxy Server Monitoring Script

Description

This Bash script monitors system resources for a SafeSquid proxy server running on a EC2 . It provides a real-time dashboard with refresh capabilities and command-line switches for viewing specific metrics.

Prerequisites :

1. VirtualBox with safesquid.iso installed

2. Bash shell

3. Standard Linux utilities (ps, df, free, netstat, ifconfig, mpstat, systemctl)

Installation:

1. Save the script as monitor.sh


2. Make it executable
      Command -  chmod +x monitor.sh

3. Ensure required utilities are installed (most are standard in Linux distributions)

Usage

Run the script with:

Command -  ./myscript.sh 


Option : 

-cpu: Display CPU usage and load average

-memory: Show memory and swap usage

-network: Display network statistics

-disk: Show disk usage with high-usage highlighting

-processes: Show process information

-services: Check status of essential services

-topapps: Show top 10 applications by resource usage

-all: Display full dashboard (default)

-h: Show help

Features : 

1. Top 10 Applications: Shows processes consuming most CPU/memory

2. Network Monitoring: Tracks connections, packet drops, and data transfer

3. Disk Usage: Displays partition usage, highlights >80% usage

4. System Load: Shows load average and CPU usage breakdown

5. Memory Usage: Displays RAM and swap statistics

6. Process Monitoring: Shows active processes and top consumers

7. Service Monitoring: Checks status of sshd, nginx/apache, iptables

8. Custom Dashboard: Refreshes every 5 seconds, supports selective viewing

Notes :

* The dashboard refreshes every 5 seconds by default
* Use Ctrl+C to exit the full dashboard
* Some commands (e.g., mpstat) may require    sysstat package
* Script assumes standard SafeSquid service configurations
