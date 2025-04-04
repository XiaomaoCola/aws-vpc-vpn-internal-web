
# 🌐 AWS VPC Internal Network + VPN Architecture Project

> Build a secure internal AWS network accessible via VPN, simulating a real-world enterprise setup.

---

## 🧠 Project Goals

This project aims to set up a complete internal network architecture on AWS that includes:

- ✅ Creating a private AWS VPC (Virtual Private Cloud)
- ✅ Deploying a VPN service for secure remote access
- ✅ Hosting an internal-only web service
- ✅ Gaining hands-on experience with cloud networking, VPN setup, and security groups
- ✅ Simulating real enterprise workflow: VPN access → internal service

---

## 📦 Project Phases

### 🚀 Phase 1: Basic Networking and VPN Setup
- [ ] Create a custom VPC (CIDR: 10.10.0.0/16)
- [ ] Create a public subnet (10.10.1.0/24)
- [ ] Launch an EC2 instance (Amazon Linux / Ubuntu)
- [ ] Install L2TP/IPSec VPN (e.g., StrongSwan or Libreswan)
- [ ] Configure Pre-shared Key + username/password authentication
- [ ] Open required ports (UDP 500, 4500)

### 🌐 Phase 2: Internal Web Service
- [ ] Deploy Nginx or similar on the same EC2 instance
- [ ] Bind web service to private IP only
- [ ] Ensure only VPN clients can access it

### 🔒 Phase 3: Security and Logging
- [ ] Configure Security Groups to restrict access
- [ ] Enable CloudWatch logs for VPN connections
- [ ] (Optional) Use Filebeat + Elasticsearch to analyze access logs

---

## 🧪 VPN Connection Test

- Use Windows built-in VPN client
- VPN Type: L2TP/IPSec with Pre-Shared Key
- Authentication: Username + Password
- After connection, access web service at http://10.10.1.10

---

## 🔧 Technologies Used

| Tech | Purpose |
|------|---------|
| AWS EC2 | Server host |
| AWS VPC | Private networking |
| StrongSwan / Libreswan | VPN server |
| Nginx | Web service |
| Windows VPN Client | Remote access test |
| CloudWatch / Filebeat | Logging & monitoring |

---

## 🧱 Architecture Diagram

```
[Your PC]──VPN──► [AWS VPN Gateway / EC2 VPN]──► [AWS VPC Private Subnet]
                                              └──► Internal Web Service (Nginx)
```

---

## 📝 Who Is This For?

- Beginners learning AWS networking
- Aspiring DevOps / SRE / Cloud Engineers
- Security learners exploring VPN & access control
- Anyone wanting a strong project on their resume 🚀

---

## 📌 TODO (Next Steps)

- [ ] Write detailed deployment guide
- [ ] Provide setup scripts (bash / cloud-init)
- [ ] Add automation with Terraform
- [ ] Add multi-user VPN support

---

## 📄 License

MIT License.

---

## ✨ Author

ZZ
Aspiring Cloud Architect & Security Engineer.
