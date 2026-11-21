# Wazuh SIEM Lab Architecture

## Objective
Build a security monitoring laboratory using Wazuh.

## Components

### 1. Wazuh Manager
- Receives security events from agents.
- Analyzes logs.
- Generates security alerts.
- Manages detection rules.

### 2. Ubuntu Victim
- Runs the Wazuh Agent.
- Generates authentication logs.
- Provides files for integrity monitoring.

### 3. Kali Linux Attacker
- Performs authorized security tests.
- Executes Nmap network scans.
- Simulates SSH brute-force attempts against the lab victim.

## Network
All laboratory machines must communicate through an isolated private network.

## Security
All tests must be performed only on systems owned by the project.
