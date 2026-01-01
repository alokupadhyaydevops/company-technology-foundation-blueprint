# IP Addressing — Public, Private, and Elastic IP

## What Is an IP Address (Simple Meaning)
An IP address is a unique numeric identifier used to locate a machine on a network.
It allows data to know where it should be delivered.

Without IP addresses, communication between systems would not be possible.

---

## Why IP Addresses Exist
Modern systems communicate over networks with millions of machines.
IP addresses provide:
- Unique identification
- Predictable routing
- Scalable communication

They are the foundation of all networking.

---

## Private IP Address (Internal Identity)
A private IP address is used for communication **inside a private network**.

In AWS:
- Every EC2 instance always has a private IP
- Private IPs are not reachable from the internet
- They remain stable for the lifetime of the instance

Private IPs are used for:
- Internal service communication
- Backend systems
- Databases

They represent the internal identity of a server.

---

## Public IP Address (Internet Identity)
A public IP address allows a server to be reachable from the internet.

In AWS:
- Public IPs are assigned dynamically by default
- They may change when an instance is stopped and started
- They are not guaranteed to remain the same

Public IPs enable external access but should not be relied on for long-term stability.

---

## Why AWS Changes Public IPs by Default
AWS manages a limited pool of public IPv4 addresses.
To optimize resource usage:
- Public IPs are released when instances stop
- New IPs may be assigned on restart

This behavior is expected and is not a mi

