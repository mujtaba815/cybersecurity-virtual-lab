# Cybersecurity Virtual Lab

A beginner-level cybersecurity virtual lab environment built using **Kali Linux, VMware, Docker, and OWASP Juice Shop**.

This repository contains the setup, configuration, verification steps, and documentation for cybersecurity practical labs.

##  Technologies Used

* Kali Linux
* VMware
* Docker
* OWASP Juice Shop
* Linux CLI
* cURL
* HTTP

## 📌 Task 01 — Cybersecurity Virtual Lab Setup

### Lab Overview

For Task 01, Kali Linux was configured as a virtual machine using VMware. Docker was installed inside Kali Linux and used to deploy **OWASP Juice Shop** as an intentionally vulnerable web application.

The Juice Shop application was deployed through a Docker container and accessed locally on **port 3000**.

### Lab Architecture

```text
┌──────────────────────────────┐
│        Host Machine          │
│          Windows             │
│                              │
│          VMware              │
│              │               │
│              ▼               │
│     ┌─────────────────┐      │
│     │    Kali Linux   │      │
│     │                 │      │
│     │     Docker      │      │
│     │        │        │      │
│     │        ▼        │      │
│     │  OWASP Juice    │      │
│     │      Shop       │      │
│     │   Port: 3000    │      │
│     └─────────────────┘      │
└──────────────────────────────┘
```

## ⚙️ Environment Setup

### 1. Kali Linux

Kali Linux was configured as a virtual machine using VMware.

The active network interface was configured with the following IP address:

```text
192.168.43.128
```

### 2. Docker Installation

Docker was installed inside Kali Linux and used as the container runtime for the vulnerable web application.

Example installation:

```bash
sudo apt update
sudo apt install docker.io
```

Verify Docker:

```bash
docker --version
```

### 3. OWASP Juice Shop

OWASP Juice Shop was deployed using Docker and configured to run on:

```text
127.0.0.1:3000
```

The application can be accessed through a web browser at:

```text
http://127.0.0.1:3000
```

### 4. Connectivity Verification

Connectivity to the Juice Shop application was verified using `curl`:

```bash
curl http://127.0.0.1:3000
```

A valid HTML response from the application confirmed that the target was running and reachable.

##  Verification

The following components were successfully verified:

* Kali Linux virtual machine running
* VMware network adapter configured
* Docker installed successfully
* OWASP Juice Shop running inside Docker
* Juice Shop accessible on port `3000`
* Kali Linux IP address identified
* HTTP connectivity verified using `curl`

##  Lab Purpose

This environment provides an isolated platform for learning and practicing cybersecurity concepts such as:

* Web application security
* HTTP traffic analysis
* Vulnerability identification
* Security testing
* Linux command-line operations
* Docker-based lab environments
* SOC and cybersecurity fundamentals

All security testing should be performed only against intentionally vulnerable applications or systems that you own or have permission to test.

##  Repository Contents

```text
Task-01-Lab-Setup/
├── screenshots/
└── Task01_Lab_Setup_Submission.pdf
```

The `Task-01-Lab-Setup` directory contains the documentation and screenshots for the initial lab setup.

##  Author

**Syed Mujtaba Hussain**

Cybersecurity Intern
Cybersecurity Fundamentals / Lab Setup

## 📄 Task Documentation

The complete Task 01 submission report is included in this repository.
