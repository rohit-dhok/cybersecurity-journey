# Nmap Basics

## Common Scans

### Service Detection

```bash
nmap -sV <target-ip>
```

Detects service versions.

### Default Scripts

```bash
nmap -sC <target-ip>
```

Runs default NSE scripts.

### Full Port Scan

```bash
nmap -p- <target-ip>
```

Scans all 65535 ports.

## Advanced Scans

### SYN Scan (Stealth Scan)

```bash
nmap -sS <target-ip>
```

Performs a TCP SYN scan to identify open ports without completing the full TCP three-way handshake.

### How It Works
1. Sends SYN packet to target
2. Receives SYN-ACK if port is open
3. Sends RST instead of ACK to terminate connection

Because the connection is not fully established, this scan is often called a "half-open" or "stealth" scan.

### Notes
- Requires root/admin privileges
- Faster than full TCP connect scans
- Some systems and IDS/IPS solutions can still detect it

## What I Learned
In pentesting, enumeration is often the most critical phase because it reveals the information that guides every step that follows. The more you learn about the target during enumeration, the easier it becomes to identify weaknesses and potential entry points.
