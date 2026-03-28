# local-vm-autoscaling-gcp
#  Local VM Auto-Scaling to GCP

##  Project Overview

This project demonstrates an automated system where a **local virtual machine monitors its CPU usage** and triggers **auto-scaling to Google Cloud Platform (GCP)** when usage exceeds a defined threshold.

---

##  Objective

* Monitor CPU usage on a local VM
* Trigger scaling when CPU > 75%
* Automatically create a VM instance in GCP
* Deploy a sample application on the cloud VM

---

## Technologies Used

* Ubuntu (Local VM)
* Python (psutil)
* Bash scripting
* Google Cloud Platform (Compute Engine)
* gcloud CLI

---

##  Implementation Steps

### 1. Local VM Setup

* Created Ubuntu VM using UTM (Mac M1 compatible)

### 2. Resource Monitoring

* Implemented Python script using `psutil`
* Continuously checks CPU usage

### 3. Load Simulation

* Used `stress` tool to simulate high CPU load

### 4. Auto Scaling Trigger

* When CPU > 75%, script triggers a Bash script

### 5. Cloud VM Creation

* Bash script uses `gcloud` CLI to create a new VM in GCP

### 6. Application Deployment

* Deploys a simple Python HTTP server on the new VM

---

##  Project Structure

```
auto-scaling-project/
│
├── monitor.py
├── scale_to_gcp.sh
├── README.md
```

---

##  How to Run

### Step 1: Start Monitoring

```
python3 monitor.py
```

### Step 2: Simulate Load

```
stress --cpu 4
```

---

##  Architecture Flow

Local VM → CPU Monitoring → Threshold Check → Trigger Script → GCP VM Creation → App Deployment

---

##  Results

* Successfully detected high CPU usage
* Automatically created VM in GCP
* Deployed application on cloud instance

---

##  Limitations

* Not real-time migration
* Delay in VM startup
* Basic automation (can be improved with Kubernetes)

---

## Future Enhancements

* Use Kubernetes Auto-scaling
* Add Grafana Dashboard
* Implement Load Balancer

---

##  Author

* Yogita
