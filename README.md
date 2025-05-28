
📦 Smart Cart with Automatic Billing System
A Smart Cart system designed using ESP32, RFID, OLED, and LCD that automates billing in retail environments. This project aims to reduce human effort, eliminate queues, and enhance user convenience during shopping.

🔧 Components Used
Component	Quantity	Description
ESP32 Dev Kit	1	Main controller with Wi-Fi & Bluetooth
RFID Reader (MFRC522)	1	Scans RFID tags for product identification
RFID Tags	n	Each tag represents an item
OLED Display (SSD1306)	1	128x64 display for total amount
I2C LCD Display (16x2)	1	For user messages
Push Buttons	3	Add, Remove, and Show Total buttons
Breadboard + Wires	-	For circuit connection
Power Supply	1	3.3V regulated (from ESP32)

🔌 Pin Connections
Component	Signal	ESP32 Pin
RFID (MFRC522)	SDA (SS)	D19
SCK	D23
MOSI	D21
MISO	D22
RST	D18
OLED (I2C)	SDA	D4
SCL	D5
I2C LCD (16x2)	SDA	D4 (shared)
SCL	D5 (shared)
Push Buttons	Add Button	D12
Remove Button	D13
Total Button	D14
Power & Ground	VCC (All modules)	3.3V
GND (All modules)	GND

Note: OLED and I2C LCD both share I2C bus (SDA/SCL).

⚙️ Working Principle
Product Scanning: Each item is assigned an RFID tag. When placed near the RFID reader, the tag is scanned.

Cart Management: The user can add or remove items using the respective buttons.

Display:

OLED: Shows the running total of added items.

LCD: Displays current action/status messages.

Billing: On pressing the 'Total' button, the complete amount is shown.

All operations are managed in real-time by the ESP32.

✅ Features
Real-time item addition/removal.

Dual-display output (item status + total price).

Simple UI using buttons.

No manual billing or cashier required
