# Task 4: Setup and Use a Firewall on Windows/Linux

## Objective
Configure and test basic firewall rules to allow or block traffic.


## Summary: How a Firewall Filters Traffic
A firewall acts as a barrier between a trusted internal network and untrusted external networks. It inspects incoming and outgoing data packets based on a predetermined set of security rules. By analyzing packet headers (which contain source/destination IP addresses and ports), it decides whether to allow, drop, or reject the traffic.

## Steps Completed
1. Opened the firewall configuration tool.
2. Documented current rules.
3. Added a rule to block inbound traffic on Port 23 (Telnet).
4. Verified the rule was applied successfully.
5. Removed the rule to restore the system's original state.

## Proof of Completion
![Firewall Rule Screenshot](rule created.png)

## Interview Question Answers

### 1. What is a firewall?
A network security device or software that monitors and filters incoming and outgoing network traffic based on an organization's previously established security policies.

### 2. Difference between stateful and stateless firewall?
* **Stateless Firewall:** Inspects packets individually based on static metrics (IP address, port) without context of the ongoing connection session.
* **Stateful Firewall:** Tracks the operating state of active network connections and handles traffic based on the context of the entire session history.

### 3. What are inbound and outbound rules?
* **Inbound Rules:** Protect the network against incoming traffic originating from outside your local machine/network.
* **Outbound Rules:** Regulate traffic originating from your local machine/network heading out to an external network.

### 4. How does UFW simplify firewall management?
UFW (Uncomplicated Firewall) provides a simplified command-line interface for complex iptables, allowing users to manage rules using natural language commands like `ufw allow` or `ufw deny`.

### 5. Why block port 23 (Telnet)?
Telnet transmits data, including passwords and usernames, in plain clear text. This makes it highly vulnerable to packet sniffing and interception, so it is blocked in favor of encrypted protocols like SSH (Port 22).

### 6. What are common firewall mistakes?
* Leaving unneeded or administrative ports wide open to the public internet.
* Ordering rules incorrectly (firewalls evaluate rules from top to bottom; a broad "allow all" rule placed early can override strict blocking rules).
* Forgetting to log and audit firewall events.

### 7. How does a firewall improve network security?
It blocks unauthorized access to system ports, prevents malicious external entities from initiating connections to sensitive local applications, and helps stop data exfiltration.

### 8. What is NAT in firewalls?
NAT (Network Address Translation) maps multiple private IP addresses within an internal network to a single public IP address before transferring packets to the internet, hiding internal network topologies from outside observation.
