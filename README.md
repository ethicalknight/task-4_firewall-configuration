# Task 4: Setup and Use a Firewall on Windows

## 🎯 Objective
Configure and test basic firewall rules using Windows Defender Firewall to allow or block traffic.

---

## 🛠 Tools Used
- **Windows Defender Firewall with Advanced Security**
- **Telnet Client (for testing)**
- **Windows GUI Interface**

---

## ✅ Steps Performed

### 1. Open Windows Firewall Configuration
- Press `Win + R`, type `wf.msc`, and press **Enter**.
- This opens **Windows Defender Firewall with Advanced Security**.

### 2. List Current Firewall Rules
- In the left pane, click on **Inbound Rules**.
- Browse or sort to view existing rules by port or name.

### 3. Add a Rule to Block Inbound Traffic on Port 23 (Telnet)
- Go to **Inbound Rules** → Click **New Rule** (right pane).
- Choose **Port** → Click **Next**.
- Select **TCP**, and enter `23` → Click **Next**.
- Select **Block the connection** → Click **Next**.
- Apply the rule to **Domain, Private, and Public** profiles → Next.
- Name the rule: `Block Telnet Port 23` → Click **Finish**.

### 4. Test the Block Rule
- Open Command Prompt and type:
  ```bash
  telnet localhost 23
