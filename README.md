<!-- GitHub Profile README for a Professional PLC & Automation Engineer -->

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/en/c/cb/Raspberry_Pi_Logo.svg" alt="Raspberry Pi" width="80"/>
</p>

<h1 align="center">Hi, I'm Abdul Karim 👋<br>Welcom to CODESYS PLC using Raspberry pi 5 </h1>

<p align="center">
  <strong>PLC Programmer | HMI & SCADA Developer | Control Panel Designer | Siemens & CODESYS Expert</strong><br>
  <i>This Repository is to build DIY PLC for LOW Cost using Raspberry PI and CODESYS for real-world automation solutions using modern industrial technologies</i>
</p>

---

## 💼 Table of Contents :
 <h1 align="center">**Hardwares**</h1>

- Raspberry Pi 5 (4GB or 8GB)
- microSD card (16GB or higher, Class 10) #Installed PI OS 64 / If not see Installation
- Power supply (USB-C, 5V 3A+)
- Ethernet cable (for stable communication)
- Breadboard
- Jumper wires
- Optional: GPIO-connected 12V push buttons, LED indicators (via relay/level shifter)
- Optional: Raspberry pi TCobbler if using breadboard
- Optional: High voltage appliances (AC/DC)
- Optional: Power Adapter (0-36V DC)
---
 <h1 align="center">**Softwares**</h1>

- Raspberry Pi OS (Lite or Desktop, 64-bit recommended)
- CODESYS Development System (on your Windows PC)
- CODESYS Control for Raspberry Pi SL (SoftPLC runtime)
- CODESYS License (free demo or paid full)
  
---
 <h1 align="center">**Installation**</h1>
 <h4>**Install Raspberry PI OS 64 into Raspberry PI 5 (RAM more than 4GB)**</h4>
 
- Rasoberry PI 5
- Micro-SD Card (atleast 64GB) 
- USB SD Card Reader

#Step 1:

- Download Raspbery pi [Imager](https://downloads.raspberrypi.org/imager/imager_latest.exe) for Windows
- Flash “Raspberry Pi OS 64-bit (Lite or Desktop)” to SD card.
- Enable SSH and Wi-Fi (if needed) using raspi-config or headless setup.
- Boot up Pi and update packages:
- Bash <i>Copy below code</i>
  
   sudo apt update && sudo apt upgrade -y
  <!--
  ![Raspberry Pi Codesys PLC Setup](https://yourdomain.com/path/to/image.png)
  ![update-pi-terminal](https://user-images.githubusercontent.com/123456789/update-pi-terminal.png) -->

#Step 2:

- Connect Pi to same local network as your PC.
- Find Pi’s IP using:
- Bash <i>Copy below code</i>
  
  hostname -I
- Keep this IP ready for CODESYS connection.

#Step 3: 

- Download [Codesys](https://store.codesys.com/en/codesys-control-for-raspberry-pi-sl.html) for Windows
- Install CODESYS Development System (PC)
  <i>(FREE version CODESYS only works for 2 hours continiously so make sure to restart Raspberry pi in every 2 hours interval)</i>
  
#Step 4:

- Install CODESYS Control for Raspberry Pi SL
  
  <h8>Which you have</h8>

  - 1st External Monitor
  - 2nd VNC Software laptop
  - 3rd Use [PUTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) on Windows

#Step 5:

- Deploy CODESYS Runtime on Raspberry Pi
  
  - On your Windows PC, open CODESYS Development System
  - Go to Tools → Device Installer
  - Install Raspberry Pi runtime:
  - Menu: Tools → Update Raspberry Pi
  - Enter your Pi IP address
  - Provide username (pi) and password (raspberry or your custom)

  It will install runtime over SSH

#Step 6:

- Activate License (optional)
  - You can run a demo version (2 hours runtime).
  - For production: Buy license from CODESYS Store and activate via License Manager.

#Step 7: 
- Create a PLC Project in CODESYS
  - File → New Project
  - Choose: Standard project (Rename it)
  - CODESYS Control for Raspberry Pi
  - Select PLC_PRG and Ladder Logic (LD) or Structured Text (ST)

- Add devices:
  - GPIO (Digital Input/Output)
  - Modbus, Ethernet/IP, etc. (if needed)
  - Map GPIOs (I/O Configuration)
  - Under “Device → Raspberry Pi GPIOs”
- Assign I/O's:
  - DI (Digital Input): GPIO pins to push buttons
  - DO (Digital Output): GPIO pins to LEDs (via relay/transistor)
#Note: Raspberry Pi uses BCM pin numbering (GPIO 17 = pin 11).

- Download & Run PLC Program:
  - Click Login → Download → Start PLC
  - Watch Live I/O values in real time

Your Raspberry Pi is now a fully running PLC using CODESYS!

---

<details>
  <summary>Hardwares List</summary>
  
- Raspberry Pi 5 (4GB or 8GB)
- microSD card (16GB or higher, Class 10) #Installed PI OS 64 / If not see Installation
- Power supply (USB-C, 5V 3A+)
- Ethernet cable (for stable communication)
- Breadboard
- Jumper wires
- Optional: GPIO-connected 12V push buttons, LED indicators (via relay/level shifter)
- Optional: Raspberry pi TCobbler if using breadboard
- Optional: High voltage appliances (AC/DC)
- Optional: Power Adapter (0-36V DC)
  
</details>

---

<details>
  <summary>Softwares</summary>
  
- Raspberry Pi OS (Lite or Desktop, 64-bit recommended)
- CODESYS Development System (on your Windows PC)
- CODESYS Control for Raspberry Pi SL (SoftPLC runtime)
- CODESYS License (free demo or paid full)
  
</details>

---
<details>
  <summary>Installation</summary>
  <details>
    <summary>1</summary>

    - Raspberry Pi OS (Lite or Desktop, 64-bit recommended)
    - CODESYS Development System (on your Windows PC)
    - CODESYS Control for Raspberry Pi SL (SoftPLC runtime)
    - CODESYS License (free demo or paid full)

  </details>
    <details>
    <summary>2</summary>

    - Raspberry Pi OS (Lite or Desktop, 64-bit recommended)
    - CODESYS Development System (on your Windows PC)
    - CODESYS Control for Raspberry Pi SL (SoftPLC runtime)
    - CODESYS License (free demo or paid full)

  </details>
    <details>
    <summary>3</summary>

    - Raspberry Pi OS (Lite or Desktop, 64-bit recommended)
    - CODESYS Development System (on your Windows PC)
    - CODESYS Control for Raspberry Pi SL (SoftPLC runtime)
    - CODESYS License (free demo or paid full)

  </details>
</details>


---
## 📁 Featured Projects

| Project       | Description      | Tech Stack |
|---------------|------------------|----------------|
|Raspberry Pi 5 Relay Control| PLC automation with Raspberrypi 5 and Codesys Runtime basic relay control, using push button and LED feedback | CODESYS, Pi 5, LD |

<h2>Bill of Materials (BOM) Example</h2>

| Item                           | Description        | Qty |
| ------------------------------ | ------------------ | --- |
| Raspberry Pi 5 (4GB)           | Main controller    | 1   |
| microSD (128GB)                | Storage            | 1   |
| USB-C PSU (5V 3A) Pi Official  | Power supply       | 1   |
| GPIO Extension Board           | Easy I/O access    | 1   |
| 12V Relay Module (16 Channel)  | For output control | 1   |
| 12V LED indicators             | For output test    | 2–4 |
| 12V Push Buttons               | For input          | 2–4 |
| 12V Level Relay                | GPIO protection    | 1   |
| Ethernet cable / WiFi          | Communication      | 1   |
| Bread Board, Jumper wires      | For Connection     | 1-10|


<i>#NOTE: I have used Active High GPIO's in Raspberry PI 5 and Active Low input Relay Channel so i have inverted my Active HIGH GPIO OUT Logic to LOW in my Code</i>
<!--| 🔄 **VFD Speed Control** | Real-time analog feedback with ramp/safety interlocks | Siemens S7-1200 + VFD |
| 🌐 **IoT Data Logger** | MQTT-based real-time SCADA integration | Raspberry Pi + Node-RED |
| 🎛 **HMI Panel Design** | Interactive SCADA dashboards with alarms, logs | WinCC + Factory I/O |
| ⚡ **Smart MCC Panel** | CAD design, PLC wiring, HMI layout & full automation | FreeCAD, TIA Portal | -->

---

## Code Snipit

## 🔌 Tech Stack

<!
### PLC & SCADA
![TIA Portal](https://img.shields.io/badge/TIA--Portal-blue?style=flat&logo=siemens)
![CODESYS](https://img.shields.io/badge/CODESYS-red?style=flat)
![WinCC](https://img.shields.io/badge/WinCC-lightgrey?style=flat&logo=windows)
![Factory I/O](https://img.shields.io/badge/Factory--IO-green?style=flat)
![OpenPLC](https://img.shields.io/badge/OpenPLC-005F9E?style=flat)
![Node-RED](https://img.shields.io/badge/Node--RED-B92829?style=flat&logo=nodered)

### Programming Languages
![Ladder Logic](https://img.shields.io/badge/Ladder--Logic-yellow?style=flat)
![Structured Text](https://img.shields.io/badge/Structured--Text-orange?style=flat)
![FBD](https://img.shields.io/badge/FBD-blueviolet?style=flat)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python)

### Control Panel & Electrical Design
![FreeCAD](https://img.shields.io/badge/FreeCAD-2E3A59?style=flat&logo=freecad&logoColor=white)
![Procreate](https://img.shields.io/badge/Procreate-111111?style=flat&logo=procreate&logoColor=white)
![QElectroTech](https://img.shields.io/badge/QElectroTech-005F87?style=flat&logo=electrical-engineering&logoColor=white)
<!-- ![AutoCAD](https://img.shields.io/badge/AutoCAD-E34F26?style=flat&logo=autodesk&logoColor=white) -->

### DevOps & Cloud Tools
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=flat&logo=github&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/-Raspberry_Pi-C51A4A?style=flat&logo=Raspberry-Pi)
![Modbus](https://img.shields.io/badge/Modbus-005f9e?style=flat)

---

## 🌐 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/abdulkarimmiddya)  
[![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:abdulkarimmiddya108@gmail.com) 

---

## 💡 GitHub Repositories

- [AbdulkarimGit-Tech](https://github.com/AbdulkarimGit-Tech/AbdulkarimGit-Tech) – Main Repositories


---

## ☕ Support My Work

[![PayPal](https://img.shields.io/badge/Donate-PayPal-blue?style=for-the-badge&logo=paypal)](https://paypal.me/abdulkarimmiddya108@gmail.com)

---

<!-- Proudly built with real-world hands-on experience. Engineering Automation, One Project at a Time. -->
