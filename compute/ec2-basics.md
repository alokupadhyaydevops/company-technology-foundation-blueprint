# EC2 Basics — Understanding Servers on AWS

## What Is a Server (Real Meaning)
A server is simply a computer that is always available to respond to requests.
Unlike personal computers, servers are designed to run continuously and provide services such as websites, APIs, or databases.

In cloud environments, servers are virtual machines running inside large data centers.

---

## Why EC2 Exists
Amazon EC2 exists to remove the need for physical servers.

Instead of:
- Buying hardware
- Managing power and cooling
- Handling physical failures

AWS provides virtual servers that can be created, resized, stopped, or terminated on demand.

This allows engineers to focus on **architecture and reliability**, not hardware.

---

## What an EC2 Instance Really Is
An EC2 instance is a virtual machine that includes:
- CPU
- Memory (RAM)
- Storage (EBS)
- Network interface

Each instance runs inside a private network (VPC) and is accessed securely.

---

## How Linux Servers Are Accessed
Linux-based EC2 instances are accessed using **SSH (Secure Shell)**.

Key points:
- Password login is disabled by default
- Access is controlled using key pairs
- SSH provides encrypted remote access

This prevents brute-force password attacks and is standard industry practice.

---

## Services vs Manual Processes
Production applications must run as **services**, not manually started commands.

Services:
- Are managed by the operating system
- Can start automatically after reboot
- Can be monitored and restarted

In this project, Nginx was configured as a service and enabled to start automatically.

---

## Common Beginner Mistakes (And How This Project Avoided Them)
- Running applications manually instead of as services
- Relying on public IPs without understanding lifecycle
- Ignoring reboot behavior
- Not verifying service status after restart

These mistakes cause real production outages.

---

## Practical Experience From This Project
In this project, the EC2 instance was:
- Launched inside a VPC
- Accessed securely using SSH
- Configured with Nginx as a web server
- Verified across reboot scenarios
- Debugged using logs and service status

This reflects real-world server management responsibilities.

---

## Key Takeaway
EC2 is not just a virtual machine.
It is the foundation on which reliable, secure, and scalable systems are built.
Understanding server behavior is critical before moving to advanced cloud services.

