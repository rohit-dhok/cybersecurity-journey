# Metasploitable Enumeration

## Objective
Perform initial enumeration against Metasploitable.

---

## Target Information

| Item | Value |
|---|---|
| Target IP | 192.168.x.x |
| Attacker Machine | Kali Linux |

---

## Host Discovery

### Ping Test

```bash
ping <target-ip>
```

Host responded successfully.

---

## Nmap Scan

### Command Used

```bash
nmap -sV -sC <target-ip>
```

### Purpose
- Detect service versions
- Run default NSE scripts

---

## Open Ports & Services

| Port | Service |             Notes              |
|------|---------|--------------------------------|
|  21  |   FTP   | Anonymous login may be enabled |
|  22  |   SSH   | Remote login service           |
|  80  |   HTTP  | Web server detected            |

Only common ports shown here.

---

## Initial Observations

- Multiple services are exposed
- Some services appear outdated
- Attack surface is large

---

## Lessons Learned

- Enumeration provides valuable information before exploitation
- Service versions may reveal vulnerabilities
- Nmap scripting adds useful context
