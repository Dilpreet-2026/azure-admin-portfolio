# Project 1: Secure Azure Virtual Machine Deployment (AZ-104)

## Project Overview

This project demonstrates my hands-on skills as an **Azure Administrator** by deploying and securing an Azure Virtual Machine following AZ-104 best practices. 
The focus is on **compute, networking, security, and troubleshooting** — core responsibilities of cloud support and admin roles.

---

## Objectives

* Deploy an Azure Virtual Machine
* Configure secure network access using NSGs
* Enable monitoring and boot diagnostics
* Apply availability and security best practices
* Validate and troubleshoot connectivity

---

## Azure Services Used

* Azure Virtual Machine
* Virtual Network (VNet)
* Subnet
* Network Interface (NIC)
* Network Security Group (NSG)
* Azure Monitor
* Boot Diagnostics

---

## Architecture Diagram (Logical)

```
User → Internet → NSG → NIC → Azure VM
```

---

## Step 1: Resource Group Creation

* Created a dedicated **Resource Group** to logically group all VM-related resources
* Region selected based on availability and cost considerations

**Why this matters:**
Resource groups simplify management, monitoring, and cleanup.

---

## Step 2: Virtual Network & Subnet

* Created a Virtual Network with a custom address space
* Created a subnet for VM placement

**Why this matters:**
VNets provide isolation and allow controlled communication between Azure resources.

---

## Step 3: Virtual Machine Deployment

* Selected appropriate VM size based on workload
* Chose OS image (Windows/Linux)
* Enabled **managed disks**
* Disabled public IP exposure where possible

**AZ-104 Focus:**

* VM sizing
* OS disk vs data disk
* Cost vs performance

---

## Step 4: Network Security Group (NSG) Configuration

* Created NSG and associated it with NIC
* Configured inbound rules:

  * Allowed RDP/SSH only from specific IP
  * Denied all unnecessary inbound traffic

**Why this matters:**
NSGs act as a firewall and are critical for VM security.

---

## Step 5: Boot Diagnostics & Monitoring

* Enabled Boot Diagnostics
* Configured Azure Monitor alerts for VM health

**Use cases:**

* VM not responding
* OS boot issues
* Performance troubleshooting

---

## Step 6: Availability & Reliability Considerations

* Evaluated Availability Set vs Availability Zone
* Chose option based on SLA and workload requirements

**AZ-104 Exam Insight:**
Availability Zones provide higher SLA than Availability Sets.

---

## Validation & Testing

* Verified VM status
* Tested RDP/SSH connectivity
* Confirmed NSG rule enforcement

---

## Troubleshooting Scenario

**Issue:** Unable to connect to VM via RDP/SSH

**Checks Performed:**

* NSG inbound rules
* NIC association
* VM power state
* Effective security rules

**Resolution:**

* Corrected NSG priority and source IP

---

## Security Best Practices Applied

* Least privilege access
* Restricted inbound ports
* Monitoring enabled
* Public exposure minimized

---

## Key Learnings

* Secure VM deployment requires networking and identity awareness
* NSG misconfiguration is a common root cause of connectivity issues
* Monitoring is essential for proactive support

---

## How This Project Maps to AZ-104

* Compute: Virtual Machines
* Networking: VNet, Subnet, NSG
* Security: Access control
* Monitoring: Azure Monitor, Boot Diagnostics

---

## Next Improvements

* Add Azure Backup
* Integrate Log Analytics Workspace
* Place VM behind a Load Balancer

---

📌 **Status:** In Progress – screenshots and validation evidence will be added after deployment.
