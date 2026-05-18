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

## What I Learned
In pentesting, enumeration is often the most critical phase because it reveals the information that guides every step that follows. The more you learn about the target during enumeration, the easier it becomes to identify weaknesses and potential entry points.
