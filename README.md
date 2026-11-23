# AWS EBS – Hands-on Practice

## Overview
Learned and practised Amazon Elastic Block Store (EBS) with AWS EC2.

## Topics Covered
- EBS Volume Creation and Attachment
- EBS Snapshots and Backups
- Cross-Region Snapshot Copy
- EBS Lifecycle Manager
- Mounting and Unmounting Volumes
- Filesystem Creation (XFS)

## Hands-on Practice
- Created and attached a 2 GiB EBS volume to EC2.
- Identified disks using `lsblk`.
- Created an XFS filesystem.
- Mounted the volume at `/mnt/ebs-data`.
- Created and verified a test file.
- Unmounted and remounted the volume.
- Verified data persistence.

## Linux Commands
```bash
lsblk
lsblk -f
sudo mkfs -t xfs /dev/nvme1n1
sudo mkdir -p /mnt/ebs-data
sudo mount /dev/nvme1n1 /mnt/ebs-data
df -hT
sudo umount /mnt/ebs-data
```

## Environment
- AWS EC2 – t3.micro
- Amazon Linux 2023
- EBS – gp3 (2 GiB)
- Filesystem – XFS

## Screenshots
## Screenshots

### 1. Filesystem Creation
![Filesystem Creation](screenshots/Screenshot%202026-11-23%20125017.png)

### 2. Volume Mounting
![Volume Mounting](screenshots/Screenshot%202026-11-23%20125023.png)

### 3. Volume Unmounting
![Volume Unmounting](screenshots/Screenshot%202026-11-23%20125007.png)

### 4. Remount Verification
![Remount Verification](screenshots/Screenshot%202026-11-23%20125029.png)


## Learning Outcome
Gained practical knowledge of AWS EBS storage management, volume attachment, mounting, unmounting, snapshots, and backup management.

**Purpose:** Building foundational AWS knowledge for future Cloud Infrastructure and High Availability projects.
