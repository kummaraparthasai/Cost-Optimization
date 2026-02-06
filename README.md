# Cloud Cost Optimization – Automated EBS Snapshot Cleanup

## 📌 Project Overview
This project focuses on **cloud cost optimization** by automatically identifying and deleting **unused Amazon EBS snapshots**.

When the script is **manually triggered**, it checks whether the EBS volumes associated with snapshots are **not attached to any EC2 instance**.  
If a volume is detached or no longer exists, its snapshots are **deleted automatically**.

---

## 🛠️ Tech Stack
- AWS EC2
- Amazon EBS
- AWS Lambda (Python)
- IAM
- boto3

---

## ⚙️ How It Works
1. The cleanup script is **manually executed**
2. Fetches all EBS snapshots owned by the account
3. Extracts the associated Volume ID for each snapshot
4. Checks whether the volume:
   - Exists
   - Is attached to any EC2 instance
5. If the volume is **not attached**, the snapshot is **deleted**
6. The execution output prints:
   - Snapshot IDs found
   - Snapshot IDs successfully deleted

---

## 📂 Project Structure
