# UFW (Uncomplicated Firewall) Command Guide

This document covers enabling, configuring, and testing firewall rules using UFW on Linux.

## Commands in Sequence

```bash
# 1. Enable UFW and make it start on boot
sudo ufw enable

# 2. Check if UFW is active
sudo ufw status

# 3. Check UFW status with rule numbers
sudo ufw status numbered

# 4. Block Telnet (port 23)
sudo ufw deny 23/tcp

# 5. Test Telnet connection to localhost (should be refused)
telnet localhost 23
telnet 127.0.0.1 23

# 6. Allow SSH (port 22)
sudo ufw allow 22/tcp

# 7. Delete the Telnet block rule
sudo ufw delete deny 23/tcp
