# **Earthing Monitoring System** ⚡  
A system for monitoring earthing voltage differences using **ZMPT101B voltage sensors** and an **ESP32 microcontroller**, with optional **Blynk** integration for remote monitoring.

![Earthing System](https://via.placeholder.com/800x400?text=Earthing+Monitoring+System)

---

## 📚 Table of Contents
- [Hardware Requirements](#-hardware-requirements)
- [Installation & Setup](#️-installation--setup)
- [How It Works](#-how-it-works)
- [Circuit Diagram](#-circuit-diagram)
- [Data Monitoring](#-data-monitoring)
- [Troubleshooting](#-troubleshooting)
- [License](#-license)
- [Useful Links](#-useful-links)

---

## **🔧 Hardware Requirements**
- 🛠 **ESP32** microcontroller  
- 🔌 **ZMPT101B** voltage sensors (2x)  
- ⚡ **Relay module** (for controlling circuits)  
- 🏗 **Jumper wires**  
- 🔋 **Power source**  

---

## **⚙️ Installation & Setup**

### **1️⃣ Install Required Libraries**
Ensure you have the following libraries installed in your **Arduino IDE**:  
- 📂 [Blynk Library](https://github.com/debjyoti71/eatrhing_monitering_system/tree/main/libraries/blynk-library-master)  
- 📂 [WiFiManager](https://github.com/debjyoti71/eatrhing_monitering_system/tree/main/libraries/WiFiManager)  
- 📂 [ZMPT101B Library](https://github.com/debjyoti71/eatrhing_monitering_system/tree/main/libraries/ZMPT101B)  

You can manually place them inside the `libraries/` folder.

---

### **2️⃣ Upload the Code**
- 🔹 Use **`Earthing_monitoring_system_with_blynk.ino`** for remote monitoring via **Blynk**.  
- 🔹 Use **`Earthing_monitoring_system_wo_blynk.ino`** for offline monitoring.  
- 🔹 To **calibrate**, upload **`calibrate.ino`** and note the **sensitivity values**.

---

### **3️⃣ Blynk Setup (Optional)**
1. **Create a new project** in [Blynk](https://blynk.io/).  
2. Add **two virtual pins**:
   - `V1` for **voltage difference**
   - `V2` for **relay status**  
3. Replace the **Blynk Auth Token** in the `.ino` file.

---

## **📊 How It Works**
- The **ZMPT101B** sensors measure **LE (Live to Earth)** and **LN (Live to Neutral)** voltages.  
- The **ESP32** calculates the **voltage difference**.  
- If the difference exceeds `5V`, the **relay is activated** to prevent unsafe conditions.  
- Sensor data is **sent to Blynk** (if enabled) for remote monitoring.

## 🔌 Circuit Diagram

![Circuit Diagram](https://github.com/debjyoti71/eatrhing_monitering_system/blob/main/Schematics/EMS.svg?raw=true)

---

## **📊 Data Monitoring**
If **Blynk is enabled**, the system sends **real-time data** to the Blynk app.  

![Blynk Dashboard](https://via.placeholder.com/800x400?text=Blynk+Dashboard)

---

## **📌 Troubleshooting**

### **🔴 WiFi Not Connecting?**  
✅ Ensure correct **SSID & Password** in the code.  
✅ Use **WiFiManager** to set credentials dynamically.  

### **⚠️ Voltage Always 0.00V?**  
✅ Check **sensor connections**.  
✅ Run **`calibrate.ino`** to get correct **sensitivity values**.  

---

## **📜 License**
This project is open-source under the **MIT License**. Feel free to modify and improve it. 🚀  

---

## **📎 Useful Links**
🔹 [ESP32 Documentation](https://docs.espressif.com/)  
🔹 [Blynk Setup Guide](https://blynk.io/)  
🔹 [GitHub Repository](https://github.com/debjyoti71/eatrhing_monitering_system)  

---

📌 **Developed by**: [Debjyoti Ghosh](https://github.com/debjyoti71) & [Biswajit Chaterjee](https://github.com/Biswajit9609)
