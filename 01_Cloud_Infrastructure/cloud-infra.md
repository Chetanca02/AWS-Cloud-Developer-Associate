# AWS Global Infrastructure

## What is AWS Global Infrastructure?

AWS Global Infrastructure is the **worldwide physical infrastructure** that AWS uses to deliver cloud services.

It consists of:

- Regions
- Availability Zones (AZs)
- Edge Locations
- Regional Edge Caches

---

## Big Picture Analogy 🌍🏙️🏢

Think of AWS like this:

- **Region** → A **City**
- **Availability Zone** → **Buildings** in that city
- **Edge Location** → **Local delivery hubs**
- **Data Center** → **Floors inside a building**

```text
World
 └── Region (City)
      └── Availability Zone (Building)
           └── Data Center (Floor)
```

---

## AWS Regions

### What is a Region?

A **Region** is a **geographical area** where AWS has multiple, isolated data centers.

### Examples

- us-east-1 (N. Virginia)
- eu-west-1 (Ireland)
- ap-south-1 (Mumbai)

---

### Key Characteristics

- Each Region is **independent**
- Data does **NOT replicate automatically** across Regions
- You choose the Region while creating resources

---

### Why Regions Matter

| Reason               | Explanation                     |
| -------------------- | ------------------------------- |
| Latency              | Closer users → faster response  |
| Compliance           | Data residency laws             |
| Pricing              | Costs vary by Region            |
| Service Availability | Not all services in all Regions |

---

### Exam Trap ⚠️

> Data is automatically replicated across regions

❌ **False**
Replication must be **explicitly configured**.

---

## Availability Zones (AZs)

### What is an AZ?

An **Availability Zone** is **one or more isolated data centers** within a Region.

### Key Points

- AZs are **physically separated**
- Connected via **high-speed, low-latency private network**
- Designed for **fault isolation**

---

### Example

```
Region: ap-south-1
 ├── ap-south-1a
 ├── ap-south-1b
 └── ap-south-1c
```

---

### Why Multiple AZs?

To achieve:

- High Availability
- Fault Tolerance

If one AZ fails → application continues running in another AZ.

---

### Analogy 🏢

- Same city
- Different buildings
- Separate power, cooling, networking

---

### Exam Keyword ⭐

> **Multi-AZ architecture**

---

## Region vs Availability Zone (Very Important)

| Feature   | Region                      | Availability Zone       |
| --------- | --------------------------- | ----------------------- |
| Scope     | Geographic area             | Within a region         |
| Isolation | Isolated from other regions | Isolated from other AZs |
| Latency   | Higher between regions      | Very low                |
| DR Use    | Disaster recovery           | High availability       |

---

## Data Centers

### What is a Data Center?

- Physical building
- Houses servers, storage, networking
- **Not exposed directly to customers**

AWS never tells:

- Exact location
- Number per AZ

---

## Edge Locations

### What is an Edge Location?

Edge Locations are **endpoints for AWS services** that **deliver content closer to users**.

### Primary Services Using Edge Locations

- Amazon CloudFront (CDN)
- AWS Shield
- AWS WAF
- Route 53 (DNS)

---

### Analogy 🚚

- Region → Central warehouse
- Edge Location → Neighborhood delivery hub

---

### Key Benefit

- Reduced latency
- Faster content delivery

---

### Exam Trap ⚠️

> EC2 instances run in Edge Locations

❌ **False**
Compute runs in **Regions/AZs**, not Edge Locations.

---

## Regional Edge Caches

### What are Regional Edge Caches?

- Larger cache locations
- Sit between Edge Locations and Regions
- Used by CloudFront

### Benefit

- Improve cache hit ratio
- Reduce load on origin servers

---

## How Traffic Flows (CloudFront Example)

```text
User
 → Edge Location
   → Regional Edge Cache
     → Origin (S3 / EC2 in Region)
```

---

## Global vs Regional vs AZ-Scoped Services

### Global Services

- IAM
- Route 53
- CloudFront
- AWS WAF (global)

---

### Regional Services

- EC2
- S3
- RDS
- Lambda
- VPC

---

### AZ-Scoped Services

- EC2 instances
- EBS volumes
- Subnets

---

### Exam Question Pattern 🧠

> Which AWS service is global?

✅ IAM
❌ EC2

---

## High Availability vs Fault Tolerance

### High Availability

- System remains available
- Minimal downtime
- Multi-AZ design

---

### Fault Tolerance

- System continues operating even if components fail
- No service interruption

---

### Analogy

- **HA** → Backup generator kicks in
- **FT** → Multiple generators already running

---

## Choosing the Right Architecture

| Requirement       | Recommended Design          |
| ----------------- | --------------------------- |
| High availability | Multi-AZ                    |
| Disaster recovery | Multi-Region                |
| Low latency       | Closest Region + CloudFront |
| Compliance        | Region-specific deployment  |

---

## Exam Rapid Fire ⚡

| Statement                            | True / False |
| ------------------------------------ | ------------ |
| AZs share power supply               | False        |
| Regions replicate data automatically | False        |
| Edge Locations run EC2               | False        |
| Multi-AZ improves availability       | True         |
| IAM is global                        | True         |

---

## Quick Memory Hook 🧠

- **Region = City**
- **AZ = Building**
- **Edge = Delivery Hub**
- **Global = Everywhere**

---
