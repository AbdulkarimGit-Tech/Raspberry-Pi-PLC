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
  <summary>Softwares Download and Install</summary>
  
- Download and Install [Raspberry Pi Imager](https://downloads.raspberrypi.org/imager/imager_latest.exe) for Windows
- Download and Install [CODESYS](https://store.codesys.com/en/codesys-control-for-raspberry-pi-sl.html) for Windows
- Download and Install [CODESYS Control for Raspberry Pi SL](https://store.codesys.com/en/codesys-control-for-raspberry-pi-sl.html) (SoftPLC runtime) for Windows
- Download and Install [PUTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) on Windows
- Download and Install [WinSCP](https://winscp.net/download/WinSCP-6.5.1-Setup.exe/download) for manual installation
- Download [CODESYS License (free demo or paid full)](https://store.codesys.com/en/codesys-control-for-raspberry-pi-sl.html)
  
</details>

---

<details>
  <summary>Installation</summary>

  &nbsp;&nbsp;&nbsp;&nbsp;
  <details>
    <summary>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Raspberry pi Setup</summary>
      &nbsp;&nbsp;&nbsp;&nbsp;
      <details>
        <summary>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Install Raspberry PI OS     </summary>
    
  <h2 align="center">Install Raspberry PI OS 64 into Raspberry PI 5 (RAM more than 4GB)</h2>
    
    - Rasoberry PI 5
    - Micro-SD Card (atleast 16GB) 
    - USB SD Card Reader 
  <!--
  -->
    
    - Open PI Imager
      - Flash “Raspberry Pi OS 64-bit (Lite or Desktop)” to SD card and config additional settings before FLASH.

<table>
  <tr>
    <td align="center">
      <sub>Open PI Imager</sub><br/>&nbsp;
      <img src="Images/PI_Imager.png" alt="PI_Imager" width="900"/>
    </td>
    <td align="center">
      <sub>Choose Device</sub><br/>&nbsp;
      <img src="Images/PI_Choose_Device.png" alt="PI_Choose_Device" width="900"/>
    </td>
    <td align="center">
      <sub>Choose OS</sub><br/>&nbsp;
      <img src="Images/PI_Choose_OS.png" alt="PI_Choose_OS" width="900"/>
    </td>
  </tr>
   <tr>
    <td align="center">
      <sub>Select Storage</sub><br/>&nbsp;
      <img src="Images/PI_Choose_Storage.png" alt="PI_Choose_Storage" width="900"/>
    </td>
    <td align="center">
      <sub>Edit Settings</sub><br/>&nbsp;
      <img src="Images/PI_Choose_Next.png" alt="PI_Choose_Next" width="900"/>
    </td>
    <td align="center">
      <sub>Configure OS</sub><br/>&nbsp;
      <img src="Images/PI_OS_Config.png" alt="PI_OS_Config" width="900" height="220"/>
    </td>
  </tr>
   <tr>
    <td align="center">
      <sub>Enable SSH and Save</sub><br/>&nbsp;
      <img src="Images/PI_Enable_SSH.png" alt="PI_Enable_SSH" width="900" height="220"/>
    </td>
    <td align="center">
      <sub>OS Writing</sub><br/>&nbsp;
      <img src="Images/PI_OS_Writing.png" alt="PI_OS_Writing" width="900"/>
    </td>
    <td align="center">
      <sub>OS Verifying</sub><br/>&nbsp;
      <img src="Images/PI_OS_Verifying.png" alt="PI_OS_Verifying" width="900"/>
    </td>
  </tr>
</table>
<h2 align="center">Once finished Remove SD Card and insert into pi 5<br> ↓ <br/>PUTTY Setup</h2>
</details>

&nbsp;&nbsp;&nbsp;&nbsp;
<details>
        <summary>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;PUTTY Setup</summary>

      Once PI OS 64/32 Installed on raspberry pi 5
        Open PUTTY and Login with raspberrypi.local -> Click OK
          - Login as: Your pi ID
          - Password: Your pi password 
          # Note password not visible
<table>
  <tr>
    <td align="center">
      <sub>PUTTY Login</sub><br/>&nbsp;
      <img src="Images/PI_PUTTY_Config_OS.png" alt="PI_OS_Writing" width="900" height="400"/>
    </td>
    <td align="center">
      <sub>PUTTY pi Login</sub><br/>&nbsp;
      <img src="Images/PI_Login_Successfully.png" alt="PI_OS_Verifying" width="900" height="400"/>
    </td>
  </tr>
</table>

        # After successfully logged in get your pi IP
        
          - ifconfig or hostname -I (Keep the IP of your PI similar like Ex: 192.168.xxx.xx)
          - sudo apt update && sudo apt upgrade -y   
 
# To Enable VNC Check below Code snippet

<p>
    <sub>sudo raspi-config<br/>↓</sub><br>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <img src="Images/PI_PUTTY_VNC_Config.png" alt="VNC_Config" width="950" height="250"/>
</p>

<p>
    <sub>Click Down Arrow key on keyboad to select "Interface Options"<br>- Use Right Arrow key on keyboard to select "SELECT" Click Enter<br> ↓</sub><br>&nbsp;
    <img src="Images/PI_VNC_Config_1.png" alt="VNC" width="700" height="400"/>
</p>

---

<p>
    <sub>- Use Down Arrow key on keyboard to select VNC<br>- Use Right Arrow key to Select the option click enter and enter again <br>↓</sub><br>&nbsp;
    <img src="Images/PI_VNC_Config_2.png" alt="VNC_Config" width="700" height="400"/>
</p>

---

<p>
    <sub>- Use Right Arrow key to Select "YES" and Enter <br>↓</sub><br>&nbsp;
    <img src="Images/PI_VNC_Enable.png" alt="VNC_Enable" width="700" height="400"/><br>
    <sub>--> To finsh the setup use Right arrow key 2 times select Finish and click Enter on keyboard</sub><br/>
</p>

<h2>To apply the changes Reboot pi: "sudo reboot"</h2>
<h2 align="center">Once Completed<br> ↓ <br/>Open VNC</h2>
</details>

&nbsp;&nbsp;&nbsp;&nbsp;
<details>
        <summary>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Connect VNC with Raspbery pi</summary>

      Open VNC on Windows
      Login with raspberrypi.local -> Click Enter
        - User: Your pi ID
        - Password: Your pi password
        - Open Terminal
        - Update Pi (sudo apt update && sudo apt upgrade -y)
        - sudo shutdown now (To Shutdown Pi)

<p>
    <img src="Images/PI_VNC_Connect_ID_Pasw.png" alt="VNC_Connect" width="700" height="400"/><br>
    <img src="Images/PI_ls.png" alt="VNC_pi_Terminal" width="700" height="400"/><br>
</p>

# Raspberry Pi is ready to use
   </details>
 </details>

  &nbsp;&nbsp;&nbsp;&nbsp;
  <details>
    <summary>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Install CODESYS Control Runtime on Raspberry pi</summary><br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <details>
        <summary>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Install CODESYS Control Runtime from Windows</summary>
    
  # Install CODESYS Control Runtime from Windows
    
    - Open CODESYS Development System on Windows
    - From CODESYS Development System:
      
      - Go to Tools → Package Manager / Codesys Installer → Browse search below listed 4 package and install
        - ✅ CODESYS Control for Raspberry Pi SL
        - ✅ CODESYS Edge Gateway for Linux
        - ✅ CODESYS Control SL Extension Package
        - ✅ CODESYS SL Deploy Tool
        
    - Boot your Pi with the OS
    - Ensure it's connected to the same network as your PC
    
    - On your Windows PC, open CODESYS Development System
    
    - Go to Tools → Device Installer
    - Install Raspberry Pi runtime:
    - Menu: Tools → Update Raspberry Pi
    - Enter your Pi IP address
    - Provide username (pi) and password (raspberry or your custom)
    
  # It will install runtime over SSH
     
     - In CODESYS → Go to:
     - Tools → CODESYS Control for Raspberry Pi → Update Raspberry Pi
     - Enter your Raspberry Pi’s IP address
     - Choose:
      - Login: pi ( Your ID or default)
      - Password: raspberry (default; change if needed)
      - Select the Demo License (free, 2-hour runtime)
      - Wait for the runtime to install — success message will appear.

  #  Activate License (optional)
    - You can run a demo version (2 hours runtime).
    - For production: Buy license from CODESYS Store and activate via License Manager.
    
  <!--
  -->
  </details>
 

  <details>
        <summary>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Manual Installation from Raspberry Pi</summary>
  
  # Manual Installation from Raspberry Pi
    Choose anyone ( I'm using VNC, you can use anyone process is same)
      
      -  External Monitor
      -  VNC Software laptop
      -  PUTTY

    - Download or Locate "CODESYS Control for Raspberry Pi SL.deb" file on Windows folder
      Ex: C:\Program Files\CODESYS 3.5.21.0\CODESYS\CODESYS Control for Raspberry PI\Delivery\raspberry

    - Open WinSCP, login with:
    - Host: Your Pi’s ip or rapberrypi.local
    - User: Your ID
    - Password: Your password
    - ✅ Drag & drop the .deb file to any folder (Ex: Downloads).
---

<p>
    <sub>WinSCP Login</sub><br/>&nbsp;
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_WinSCP_Login.png" alt="WinSCP_Login"/>
</p>

---

<p>
    <sub>Locate ".deb" file into your PC, Drag & Drop into pi Folder "Downloads"</sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <img src="Images/PI_WinSCP_Find_.deb_File_Copy.png" alt="WinSCp_Copy"/>
</p>

---

<p>
    <sub>After Successfully Copied ".deb" file into pi folder</sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <img src="Images/PI_WinSCP_.deb_File_Copy.png" alt="WinSCP_Copied"/>
</p>

---
  
  # Follow Below Step to Install and Run CODESYS Runtime Successfully
        Open PuTTY / VNC:
          - Enter ip of your Raspberry Pi
          - Login:
            - Username: Your ID
            - Password: Your password

        # PI Comand line (Update pi if needed "sudo apt update && sudo apt upgrade -y")
        - Locate The copied file .deb (Use below command)
        
            > ls (Pi folders)

            > cd Downloads (Copied file folder: you can "cd" where you have copied the ".deb" file)
            
            > ls (You will see .deb file Ex: codesyscontrol_raspberry_4.15.0.0_all.deb)
            
            > sudo dpkg -i [codesyscontrol_raspberry_4.15.0.0_all.deb] ( [] Rename with yours file name)

            > sudo systemctl status codesyscontrol (Check PLC Status Active or Dead)

            > cd (Come back to Starting section)

            > sudo systemctl start codesyscontrol (manual Start PLC Runtime)

            > sudo systemctl status codesyscontrol (#it will show Active)

            > sudo systemctl stop codesyscontrol (#it will stop PLC)
            
  <h3>My PLC already Running so i Turned it Off then Turned it On</h3>    
  
  ![VNC_PI_PLC](Images/PI_PLC_Runtime_Install%20and%20Run.png)
  
  # Congrats you have successfully installed CODESYS Runtime into your pi 5
  </details>
  </details>
</details>

---

<details>
  <summary>PLC Project creation</summary><br/>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

  <details>
    <summary>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Create a New PLC Project</summary><br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

  # Create a New PLC Project
      Go to: File → New Project → Standard Project
      Select device:
        CODESYS Control for Raspberry Pi 64 SL (64 bit)
        Choose programming language: Ladder Diagram (LD), ST, etc.

<p>
    <sub>Project Creation: Go to: File → New Project → Standard Project</sub><br/>&nbsp;
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_Project_Creation.png" alt="WinSCP_Login"/>
</p>

---

<p>
    <sub>Select the Device :<br> If no Hardware : WIN v3 64 <br> If using pi 64 : pi 64 SL </sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_Project_Hardware_v.png" alt="WinSCp_Copy"/>
</p>

---

<p>
    <sub>Choose the logic lagnuage: I'm using "LD"</sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_Project_language.png" alt="WinSCP_Copied"/>
</p>

---

<p>
    <sub>Programming Environment</sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <br>Left side Device's/ POU's/ Modules | Middle LD logic page | Right side LD logic Tools | Upper side Menu &nbsp;<br/>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_Package_Environment.png" alt="WinSCP_Copied"/>
</p>

</details>

  <details>
    <summary>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Setup PLC Development Environment without Raspberry pi</summary><br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

# Setup PLC Development Environment without Raspberry pi

      - If no hardware select Simulation 
      - Click login -> Click Start
      - If have hardware no need to select Simulation

<p>
    <sub> After  Writing Logic Go to : File → Save → Generate Code (F11) to Compile <br> Down side you can see if there is any Error or Not</sub><br/>&nbsp;
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_LED_Compile.png" alt="WinSCP_Login"/>
</p>

---

<p>
    <sub>After Compilation Go to : Online → Click Simulation → Click Login</sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_LED_Simulation.png" alt="WinSCp_Copy"/>
</p>

---

<p>
    <sub>You'll see Application in Stop Mode To Run the Code : Ciick on ▶ Play button</sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_LED_Login.png" alt="WinSCP_Copied"/>
</p>

---

<p>
    <sub>You'll see Application in Run Mode <br></sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_LED_Run%20Mode.png" alt="WinSCP_Copied"/>
</p>

---

<p>
    <sub>To Change the I/O's : click on → Prepfered value it will show TRUE / FALSE : Click Ctrl + F7 to change the Input state</sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_LED_ladder.png" alt="WinSCP_Copied"/>
</p>

---

<p>
    <sub>You can see the Output Change : <br> Output LED Turned ON</sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_LED_NO-LED.png" alt="WinSCP_Copied"/>
</p>

---

<p>
    <sub>Again click on → Prepfered value it will show TRUE / FALSE : Click Ctrl + F7 to change the Input state</sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_LED_ON-OFF-LED.png" alt="WinSCP_Copied"/>
</p>

---

<p>
    <sub>You can see the Output Change : <br> Output LED Turned OFF</sub><br/>&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Images/PI_CODESYS_LED_OFF.png" alt="WinSCP_Copied"/>
</p>

  </details>

  <details>
    <summary>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Setup PLC Development Environment for Raspberry pi</summary><br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

  # Setup PLC Development Environment for Raspberry pi

    Go to: PLC PRG(PRG): Write down your PLC code -> Save it -> Click Generate code to compile

    - Add devices:
      - GPIO (Digital Input/Output)
      - Modbus, Ethernet/IP, etc. (if needed)
      - Map GPIOs (I/O Configuration)
      - Under “Device → Raspberry Pi GPIOs”
    
    Go to: GPIO's ->
    
     - GPIO parameters 
        -  Select GPIO's as INPUT or OUTPUT
     - GPIO Maping 
      - Select the lader logic variable (click on 3 dot go to PLC program and select) correspond to GPIO

        - Assign I/O's:
          - DI (Digital Input): GPIO pins to push buttons
          - DO (Digital Output): GPIO pins to LEDs (via relay/transistor/pi GPIO's)
      #Note: Raspberry Pi uses BCM pin numbering (GPIO 17 = pin 11).
      
    Go to: Tools -> Deploy Control SL -> Give ip adress, User name, password and connect CODESYS with PI
    Go to: Device -> Scan network -> elect raspberry pi ip -> Click ok
    Go to: Windows Taskber Show Hiden Icons -> right click on .64 -> Start PLC

    Go to: Tools -> Online -> Login -> click Start (F5) to Run
    
      - If no hardware select Simulation 
      - Click login -> Click Start
      - If have hardware no need to select Simulation


  # Your Raspberry Pi is now a fully running PLC using CODESYS!

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
| GPIO TCobbler Board            | Easy I/O access    | 1   |
| 12V Relay Module (16 Channel)  | For output control | 1   |
| 12V LED indicators             | For output test    | 2–4 |
| 3.3V Push Buttons              | For input          | 2–4 |
| 12V power supply               | Relay & LED power  | 1   |
| Ethernet cable / WiFi          | Communication      | 1   |
| Bread Board, Jumper wires      | For Connection     | 1-10|

[▶️ Watch the video](https://github.com/AbdulkarimGit-Tech/Raspberry-Pi-PLC/blob/380e6ad52285033cf51c794ff301bf7d8a179ed5/Project/Pi_PLC_Working.mp4)

# Hardware Circuit <br/>&nbsp;
<p>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Project/PI_PLC_Hardware_Circuit.png" alt="Hardware Circuit"/>
</p>

---

 # Hardware Wiring <br/>&nbsp;
<p>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Project/PI_PLC_Hardware_Wiring.jpg" alt="PI_PLC_Wiring"/>
</p>

---


<h2>Hardware Connection</h2>

<div style="border: 2px solid #ccc; border-radius: 10px; padding: 10px; overflow-x: auto;">
  
<table>
  <thead>
    <tr>
      <th>Connection</th>
      <th></th>
      <th>Connection</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Raspberry pi VCC</td><td>5v</td><td>Relay Channel</td><td>5v</td></tr>
    <tr><td>Raspberry pi GND</td><td>GND</td><td>Relay Channel</td><td>GND</td></tr>
    <tr><td>Raspberry pi GPIO</td><td>23</td><td>Relay Channel</td><td>IN 7</td></tr>
    <tr><td>Raspberry pi GPIO</td><td>24</td><td>Relay Channel</td><td>IN 6</td></tr>
    <tr><td>Raspberry pi GPIO</td><td>3.3v</td><td>4x4 PB Matrix</td><td>R 1</td></tr>
    <tr><td>Raspberry pi GPIO</td><td>17</td><td>4x4 PB Matrix</td><td>C 1</td></tr>
    <tr><td>Raspberry pi GPIO</td><td>18</td><td>4x4 PB Matrix</td><td>C 2</td></tr>
    <tr><td>Raspberry pi GPIO</td><td>22</td><td>4x4 PB Matrix</td><td>C 3</td></tr>
    <tr><td>Raspberry pi GPIO</td><td>27</td><td>4x4 PB Matrix</td><td>C 4</td></tr>
    <tr><td>Relay Channel VCC</td><td>12v</td><td>12v Power Supply</td><td>VCC</td></tr>
    <tr><td>Relay Channel GND</td><td>GND</td><td>12v Power Supply</td><td>GND</td></tr>
    <tr><td>Relay Channel D7</td><td>NO</td><td>Connected to Green LED +ve</td><td>12v</td></tr>
    <tr><td>Relay Channel D7</td><td>COM</td><td>Connected to 12v Power VCC + D6 COM</td><td>12v</td></tr>
    <tr><td>Relay Channel D6</td><td>NO</td><td>Connected to Red LED +ve</td><td>12v</td></tr>
    <tr><td>Relay Channel D6</td><td>COM</td><td>Connected to 12v Power VCC + D7 COM</td><td>12v</td></tr>
    <tr><td>12v Green LED</td><td>GND</td><td>Connected to 12v Power GND + D6 COM</td><td>12v</td></tr>
    <tr><td>12v Red LED</td><td>GND</td><td>Connected to 12v Power GND + D6 COM</td><td>12v</td></tr>
  </tbody>
</table>

</div>

---

# PLC Ladder Logic ex:

<p>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <br><img src="Project/PI_PLC_ladder_logic.png" alt="PLC Ladder Logic"/>
</p>

---

<i>#NOTE: I have used Active High GPIO's in Raspberry PI 5 and Active Low input Relay Channel so i have inverted my Active HIGH GPIO OUT Logic to LOW in my Code</i>

---

## Code Snipit

## 🔌 Tech Stack

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
