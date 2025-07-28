# azure-resource-locks-lab

## 📘 Overview
This lab demonstrates the use of **Azure resource locks** to protect virtual machines and resource groups from accidental modification or deletion within the Azure Portal.

## 🛠️ Lab Setup
- **Resource Group**: `rg_eastus_262385_1_173853034820`
- **Virtual Machine**: `WhizlabVM` (Ubuntu Server 20.04 LTS, Standard_B2s)
- **Authentication**: Username: `WhizlabUser`, Password: `User@1234567`
- **Disk Type**: Standard SSD (LRS)

## 🔐 Resource Locking Walkthrough

### 1️⃣ Add Delete Lock
- Navigate to WhizlabVM > **Locks**
- Add lock:  
  - Name: `WhizDel`  
  - Type: `Delete`
- Attempting to delete the VM results in: `Failed to delete` ✅

### 2️⃣ Add Read-only Lock (Resource Group)
- Navigate to Resource Group > **Locks**
- Add lock:  
  - Name: `WhizRead`  
  - Type: `Read-only`
- Attempted VM deletion: allowed after removing locks

### 3️⃣ Remove Locks and Clean Up
- Delete VM successfully after unlocking
- Delete resource group after unlocking

## ✅ Validation
Final lab status: **Passed**  
Resources were deleted only after lock removal — confirming lock enforcement.

## 🚀 What This Shows
- Awareness of **accidental deletion safeguards**
- Familiarity with **Azure governance features**
- Ability to configure **access control mechanisms** via the Portal
