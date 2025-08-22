# Lab 7-1: Local Component Demo

## คำอธิบาย
การทดลองนี้แสดงการใช้งาน component ที่มีอยู่ในโฟลเดอร์ `components/Sensors/` ของ project


## สรุปคำสั่งที่ใช้ และผลลัพธ์ที่ได้
### คำสั่งที่ใช้
```bash
# เข้าไปใน project directory
cd lab7-1_Managed_Local_Component

#export environment เพื่อให้สามารถเรียกใช้ idf tools ได้
. $IDF_PATH/export.sh

# กำหนด target ESP32
idf.py set-target esp32

# Build project
idf.py build

# (ถ้าทดสอบด้วย QEMU)
idf.py qemu monitor

```
### ผลลัพธ์ที่ได้
```bash
I (10105) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (10105) SENSOR: 🌡️  Temperature: 30.7 °C
I (10105) SENSOR: 💧 Humidity: 93.3%
I (10105) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (10105) SENSOR: 📈 All sensors operating normally
I (10105) LAB7-1: ----------------------------
I (13105) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (13105) SENSOR: 🌡️  Temperature: 3 1.7°C
I (13105) SENSOR: 💧 Humidity: 79.8%
I (13105) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (13105) SENSOR: 📈 All sensors operating normally
I (13105) LAB7-1: ----------------------------
I (16105) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (16105) SENSOR: 🌡️  Temperature: 32.6 °C
I (16105) SENSOR: 💧 Humidity: 85.0%
I (16105) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (16105) SENSOR: 📈 All sensors operating normally
I (16105) LAB7-1: ----------------------------     
I (19105) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (19105) SENSOR: 🌡 ️  Temperature: 26.0°C
I (19105) SENSOR: 💧 Humidity: 69.5%
I (19105) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (19105) SENSOR: 📈 All sensors operating normally
I (19105) LAB7-1: ----------------------------
```

### 2. นำโค้ดจาก main.c ในใบงานที่ 6 มาใช้ แล้ว build พร้อมทดสอบ
ใส่ผลลัพธ์ทั้งหมดในไฟล์ README.md ของใบงานนี้
```bash
I (9534) MAIN: === Loop 1 ===
I (9534) DISPLAY: 🧹 Screen cleared from file:  /project/components/Display/display.c, line: 28
I (9534) DISPLAY: ✨ Display ready for new content
I (9534) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (9534) SENSOR: 🌡️   Temperature: 34.6°C
I (9534) SENSOR: 💧 Humidity: 79.8%
I (9534) DISPLAY: 📊 Data display from file: /project/components/Display/display.c, line: 21
I (9534) DISPLAY: 📈 Value 1: 27.50
I (9534) DISPLAY: 📉 Value 2: 62.00
I (11534) MAIN: === Loop 2 ===
I (11534) DISPLAY: 🧹 Screen cleared from file: /project/ components/Display/display.c, line: 28
I (11534) DISPLAY: ✨ Display ready for new content
I (11534) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (11534) SENSOR: 🌡️  Temperature: 2 6.2°C
I (11534) SENSOR: 💧 Humidity: 62.4%
I (11534) DISPLAY: 📊 Data display from file: /project/components/Display/display.c, line: 21
I (11534) DISPLAY: 📈 Value 1: 28.50
I (11534) DISPLAY: 📉 Value 2: 63.00
I (11534) SENSOR: ✅ Sensor status check from file: /project/components/Sensors/sensor.c, line: 30
I (11534) SENSOR: 📈 All sensors operating normally
I (11534) DISPLAY: 📢 Displaying from file: /project/components/Display/display.c, line: 15
I (11534) DISPLAY: 📺 Message: Status Check Complete
I (13534) MAIN: === Loop 3 ===
I (13534) DISPLAY: 🧹 Screen cleared from file: / project/components/Display/display.c, line: 28
I (13534) DISPLAY: ✨ Display ready for new content
I (13534) SENSOR: 📊 Reading sensor data from file: /project/components/Sensors/sensor.c, line: 18
I (13534) SENSOR: 🌡️  Temperature: 26.6°C
I (13534) SENSOR: 💧 Humidity: 81.6%
I (13534) DISPLAY: 📊 Data display from file: /project/components/Display/display.c, line: 21
I (13534) DISPLAY: 📈 Value 1: 29.50
I (13534) DISPLAY: 📉 Value 2: 64.00
```