# SDWAN-LAB on EVE-NG

This repository provides a fully functional **Cisco SD-WAN lab environment** designed to run on [EVE-NG](https://www.eve-ng.net/). The lab simulates a realistic SD-WAN deployment including vManage, vSmart, vBond, Edge routers, and WAN/Internet transport.

## 🧱 Lab Topology

The lab includes:

- **1x vManage**
- **1x vBond**
- **1x vSmart**
- **2x vEdge/CSR Routers**
- **1x WAN transport cloud**
- **1x Internet cloud**
- **1x LAN switch / client**

All devices are interconnected using EVE-NG’s virtual bridges and emulate real-world SD-WAN connections.

## 📂 Folder Structure

SDWAN-LAB/
├── Topology/ # EVE-NG topology file (.unl or .yaml)
├── Images/ # Required VM images (not included)
├── Configs/ # Initial bootstrapping config files
├── Licenses/ # Smart Account & Viptela cert/license details (if any)
├── Screenshots/ # Topology visuals or demo proof
└── README.md


## ⚙️ Requirements

- **EVE-NG (Community or Pro)**
  - Nested virtualization enabled
  - Sufficient resources (min. 16+ GB RAM, 6+ vCPUs)
- Cisco SD-WAN images:
  - `vmanage`, `vbond`, `vsmart`, and `vedge` (CSR or vEdge)
- License files or Smart Account access (for full config)
- Internet access (optional, for software/image download)

## 🛠️ Getting Started

### 1. Upload Images to EVE-NG

Follow EVE-NG documentation to add Cisco SD-WAN images:

- `/opt/unetlab/addons/qemu/`
- Use appropriate naming: `vmanage`, `vbond`, `vsmart`, etc.
- Convert and fix permissions:
  ```bash
  /opt/unetlab/wrappers/unl_wrapper -a fixpermissions

2. Import the Topology
Copy the .unl or .yaml topology file to your EVE-NG lab directory:
/opt/unetlab/labs/SDWAN-LAB/

3. Configure Devices
Access device consoles via the EVE-NG web interface

Apply the base config from the Configs/ folder

Use bootstrap templates for vManage onboarding


