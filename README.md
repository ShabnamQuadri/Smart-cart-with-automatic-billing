# 🛒 Smart Cart with Automatic Billing System

## 🎯 **Project Overview**
This is a real-time automated billing system built using the **ESP32 microcontroller**, an **RFID reader (MFRC522)**, an **OLED display**, an **I2C LCD**, and **push buttons**. It allows customers to **add/remove items using RFID tags** and calculates the total instantly—**eliminating the need for manual billing or cashier interaction**.

---

## 🛠️ **How It Works**
- Each item is tagged with an **RFID tag** that contains a unique ID.
- When the tag is brought near the **RFID reader (MFRC522)**, the **UID is read and matched** with a product.
- The **ESP32** processes this data, and:
  - The **OLED Display (SSD1306)** shows the **current total price**.
  - The **I2C LCD** displays **status messages** (`Item Added`, `Removed`, etc.).
- Three push buttons allow the user to:
  - **Add** an item.
  - **Remove** an item.
  - **Show Total** for billing.
- The system **updates displays and memory in real time**.

---

## 💡 **Features**
- ✅ Real-time item tracking and total price updates  
- 🖥️ Dual display (OLED + LCD) for better user interaction  
- 🔘 Push-button interface for full user control  
- 🚫 No need for a cashier or manual input  
- 📱 Easily expandable with Wi-Fi, payment, or mobile app support  

---

## 🧰 **Components Used**

| **Component**            | **Description**                        |
|--------------------------|----------------------------------------|
| ESP32 Dev Kit Module     | Main microcontroller with Wi-Fi + Bluetooth |
| MFRC522 RFID Reader      | Reads RFID tags                        |
| SSD1306 OLED Display     | Shows total price                      |
| 16x2 I2C LCD Display     | Shows messages/status                  |
| Push Buttons (x3)        | Add / Remove / Show Total              |
| RFID Tags                | Unique tag per item                    |
| Breadboard + Jumper Wires | For wiring                             |

---

## 🔌 **Wiring Overview**

### 🔗 **RFID MFRC522 to ESP32 (SPI Interface)**

| **MFRC522 Pin** | **ESP32 Pin** |
|------------------|---------------|
| SDA              | D19           |
| SCK              | D23           |
| MOSI             | D21           |
| MISO             | D22           |
| RST              | D18           |
| 3.3V             | 3.3V          |
| GND              | GND           |

---

### 🖥️ **OLED Display (I2C - SSD1306) and 16x2 LCD (I2C)**

| **I2C Pin** | **ESP32 Pin** |
|-------------|---------------|
| SDA         | D4            |
| SCL         | D5            |
| VCC         | 3.3V          |
| GND         | GND           |

> **Note**: Both OLED and LCD share the **same I2C lines** (SDA & SCL).

---

### 🔘 **Push Buttons**

| **Button**     | **ESP32 GPIO** |
|----------------|----------------|
| Add Item       | D12            |
| Remove Item    | D13            |
| Show Total     | D14            |

---

## ✅ **Advantages**
- 📶 Contactless billing system  
- ⏱️ Reduces queue and billing time  
- 💸 Modular, low-cost design using open-source hardware  
- 🖥️ Dual display for enhanced UI/UX  
- 🔄 Supports real-time updates and offline operation  
