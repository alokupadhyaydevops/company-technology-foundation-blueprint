# EBS Lifecycle — Understanding Data Persistence on AWS

## What Is Storage? (Simple Meaning)
Storage is a place where data remains available even when a system is powered off.

If data disappears after a restart, it was not stored on disk.

Understanding storage behavior is critical to prevent data loss.

---

## RAM vs Disk (Critical Difference)

### RAM (Memory)
- Extremely fast
- Temporary
- Data is lost on reboot or stop

RAM is used to run applications and processes.

### Disk (Storage)
- Slower than RAM
- Persistent
- Data survives reboots

Disk is used to store files, applications, and databases.

---

## What Is EBS?
Elastic Block Store (EBS) is the disk storage used by EC2 instances.

Key points:
- Every EC2 instance uses at least one EBS volume
- The operating system lives on EBS
- Application and website files are stored on EBS

Without EBS, an EC2 instance cannot boot.

---

## What Happens During a Reboot
When an EC2 instance is rebooted:
- RAM is cleared
- EBS data remains intact

Files stored on disk remain available after reboot.

---

## What Happens During Stop and Start
When an EC2 instance is stopped and started:
- RAM is cleared
- Public IP may change
- EBS data remains intact

Applications and files stored on EBS are preserved.

---

## What Happens During Termination
When an EC2 instance is terminated:
- The instance is permanently deleted
- By default, the root EBS volume is also deleted

If no backup exists, all data is lost permanently.

---

## Common Data Loss Scenario
A common incident occurs when:
- An engineer terminates an instance
- Assumes data will remain
- The EBS volume is deleted automatically

This results in irreversible data loss.

---

## Real-World Engineering Perspective
Experienced engineers always:
- Know where data is stored
- Understand storage lifecycle
- Use backups or snapshots
- Never assume data safety without verification

Storage mistakes are one of the most expensive failures.

---

## Key Takeaway
EBS provides persistent storage for EC2 instances.
Data survives reboot and stop/start but not termination by default.
Understanding storage lifecycle is essential to protect production data.

