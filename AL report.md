# ESP32 RFID Attendance Logger - Project Report

## 1. Introduction
The **ESP32 RFID Attendance Logger** is an automated system that records attendance using **RFID technology**. It reads unique RFID tag IDs and logs attendance data into a **Google Spreadsheet** via WiFi. This project replaces traditional manual methods with an efficient, digital solution.

## 2. Objectives
- Automate attendance tracking using RFID.
- Log data to **Google Sheets** for easy access and analysis.
- Ensure a **low-cost, scalable, and user-friendly** solution.

## 3. Components Used

### **Hardware Components**
-  **ESP32 Development Board** – A microcontroller with built-in WiFi and Bluetooth.
-  **RFID-RC522 Module** – Reads RFID tag information.
-  **RFID Tags** – Unique IDs assigned to individuals.
-  **Power Supply** – 5V 2A recommended.

![ESP32 RFID Attendance Logger](https://i.imgur.com/v8I3v5u.jpeg)


### **Software Components**
-  **Arduino IDE** – For coding and uploading to ESP32.
-  **Google Apps Script** – Connects ESP32 to Google Sheets.
-  **Google Sheets** – Stores attendance records.
-  **Libraries Used**:
  - `WiFi.h` (WiFi connectivity)
  - `HTTPClient.h` (HTTP communication)
  - `MFRC522.h` (RFID handling)
  - `SPI.h` (SPI communication)

## 4. System Design
The system workflow:
1. The **ESP32** initializes WiFi and the **RFID module**.
2. When an RFID tag is scanned, the **UID (Unique ID)** is read.
3. The ESP32 **sends the UID** to a **Google Apps Script** via **HTTP request**.
4. The **script processes** the request and logs the data in **Google Sheets**.
5. The response from **Google Sheets** is displayed on the **Serial Monitor**.
![](https://i.imgur.com/M4ujgJ2.jpeg)

## 5. Working Principle
1. **RFID Scanning**  
   - User taps an RFID tag on the **RFID-RC522 module**.
2. **WiFi Communication**  
   - ESP32 connects to the internet and sends the UID.
3. **Data Logging to Google Sheets**  
   - UID, timestamp, and user details are logged.
4. **Response Handling**  
   - Serial monitor provides feedback.

## 6. Code Implementation and Google Apps Script
https://github.com/jagrutiii/attendencelogger/tree/main


## 7. Advantages
- Automated Logging:    Eliminates manual entry errors.
- Cloud Storage: Google Sheets offers real-time access.
- Scalability: Can handle multiple users and RFID tags.
## 8. Challenges & Solutions


| **Challenge**                 | **Solution**                                         |
|--------------------------------|-----------------------------------------------------|
|  **WiFi Connectivity Issues** | Ensure a stable internet connection and reliable power source. |
|  **RFID Read Errors**         | Use high-quality RFID tags and maintain proper reader distance. |
|  **Data Loss**                | Implement data retry mechanisms to prevent missing entries. |

## 9. Conclusion
The ESP32 RFID Attendance Logger is a reliable and cost-effective system for attendance tracking. It simplifies record-keeping and enhances security while utilizing cloud-based data storage.
***
