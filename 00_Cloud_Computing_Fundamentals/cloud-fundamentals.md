# AWS Cloud Fundamentals

## What is Cloud Computing?

Cloud computing is the **on-demand delivery of IT resources** (servers, storage, databases, networking, software) **over the internet**, with **pay-as-you-go pricing**.

### Simple Analogy 🏠

- **On-premises**: Buying your own house
- **Cloud**: Renting a fully furnished apartment where landlord handles maintenance

You:

- Don’t buy hardware
- Don’t manage power, cooling, repairs
- Pay only for what you use

---

## Traditional IT vs Cloud

| Aspect       | Traditional (On-Prem) | Cloud                |
| ------------ | --------------------- | -------------------- |
| Cost         | High upfront (CapEx)  | Pay-as-you-go (OpEx) |
| Scaling      | Slow, manual          | Fast, automatic      |
| Maintenance  | Your responsibility   | AWS responsibility   |
| Availability | Single data center    | Multi-region         |
| Deployment   | Weeks / Months        | Minutes              |

---

## Types of Cloud Computing

### 1. Infrastructure as a Service (IaaS)

You manage OS and above.

**Examples**

- Amazon EC2
- Amazon EBS
- VPC

**Analogy**

> Renting an empty flat – you bring furniture and manage everything inside.

---

### 2. Platform as a Service (PaaS)

AWS manages OS and runtime.

**Examples**

- AWS Elastic Beanstalk
- AWS RDS

**Analogy**

> Renting a furnished flat – walls, plumbing already done.

---

### 3. Software as a Service (SaaS)

You just use the software.

**Examples**

- Amazon WorkMail
- Amazon Chime

**Analogy**

> Staying in a hotel – just use it.

---

## Cloud Deployment Models

### Public Cloud

- Infrastructure shared among customers
- Owned by AWS

**Example**

- AWS EC2, S3

---

### Private Cloud

- Dedicated infrastructure
- Usually on-prem

---

### Hybrid Cloud

- On-prem + AWS

**Use case**

- Data residency
- Gradual migration

---

## Advantages of Cloud Computing

### 1. Trade Capital Expense for Variable Expense

No upfront hardware cost.

**Exam keyword**: *OpEx instead of CapEx*

---

### 2. Massive Economies of Scale

AWS buys hardware cheaper → you pay less.

---

### 3. Stop Guessing Capacity

Scale up/down instantly.

---

### 4. Increase Speed & Agility

Launch resources in minutes.

---

### 5. Go Global in Minutes

Deploy apps worldwide easily.

---

## Shared Responsibility Model ⭐ (VERY IMPORTANT FOR EXAM)

### Concept

Security and responsibility is **shared** between AWS and the customer.

### Visual Thinking

```
AWS: "Security OF the Cloud"
You: "Security IN the Cloud"
```

---

### AWS Responsibilities

- Data centers
- Physical security
- Hardware
- Networking infrastructure

---

### Customer Responsibilities

- OS patches
- Application security
- IAM users & permissions
- Data encryption

---

### Example Question Trap ⚠️

> Who is responsible for patching EC2 OS?

✅ **Customer**

> Who is responsible for physical server security?

✅ **AWS**

---

## Cloud Economics Summary

| Concept           | Meaning                   |
| ----------------- | ------------------------- |
| CapEx             | Upfront cost (on-prem)    |
| OpEx              | Pay as you go (cloud)     |
| Elasticity        | Scale automatically       |
| Scalability       | Increase capacity         |
| Fault Tolerance   | Continue despite failures |
| High Availability | Minimize downtime         |

---

## Exam Focus Keywords (Remember These)

- Pay-as-you-go
- Elasticity
- High availability
- Fault tolerance
- Shared Responsibility Model
- Global infrastructure

---

## Quick Self-Check ✅

- Can you explain cloud to a non-tech person?
- Do you know who patches EC2 OS?
- Do you know difference between elasticity & scalability?

---
