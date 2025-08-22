# Lab 7-3: Custom ESP32 Components (Sensor + Display)

## คำอธิบาย
การทดลองนี้แสดงการสร้าง component ใหม่ด้วยคำสั่ง `idf.py create-component`
สร้าง 2 components:
1. **Sensor Component** - อ่านค่า temperature, humidity และคำนวณ heat index
2. **Display Component** - แสดงผลข้อมูลในรูปแบบตาราง

## โครงสร้างโฟลเดอร์หลังใช้ create-component
```markdown
lab7-3_esp32_Component/
├── CMakeLists.txt
├── components/
│   ├── sensor/
│   │   ├── CMakeLists.txt
│   │   ├── include/
│   │   │   └── sensor.h
│   │   └── sensor.c
│   └── display/
│       ├── CMakeLists.txt
│       ├── include/
│       │   └── display.h
│       └── display.c
├── main/
│   ├── CMakeLists.txt
│   └── lab7-3.c
├── build/
└── README.md
```

## ผลลัพธ์ที่คาดหวัง
```bash
I (20569) LAB7-3: 📋 Reading #2
I (20569) DISPLAY: 🧹 Disp lay cleared
I (20569) DISPLAY: 
I (20569) ENHANCED_SENSOR: 🌡️  Temperature: 20.00°C
I (20569) ENHANCED_SENSOR: 💧 Humidity: 40.30%
I (20569) LAB7-3: 🔥 Heat Index: 40.15
I (20569) DISPLAY: ┌─────────────────────────────────┐
I (20569) DISPLAY: │        SENSOR DATA DISPLAY      │
I (20569) DISPLAY: ├─────────────────────────────────┤
I (20569) DISPLAY: │ 🌡️  Temperature:  20.0 0°C      │
I (20569) DISPLAY: │ 💧 Humidity:     40.30%       │
I (20569) DISPLAY: │ 🔥 Heat Index:   40.15        │
I (20569) DISPLAY: └─────────────────────────────────┘
I (20569) DISPLAY: ┌─────────────────────────────────┐
I (20569) DISPLAY: │         SYSTEM STATUS           │
I (20579) DISPLAY: ├─────────────────────────────────┤
I (20579) DISPLAY: │ Status: ✅ Comfortable         │
I (20579) DISPLAY: └─────────────────────────────────┘
I (20579) LAB7-3: ==========================================
I (26579) LAB7-3: 📋 Reading #3
I (26579) DISPLAY: 🧹 Display cleared
I (26579) DISPLAY: 
I (26579) ENHANCED_SENSOR: 🌡️  Temperature : 21.10°C
I (26579) ENHANCED_SENSOR: 💧 Humidity: 50.30%
I (26579) LAB7-3: 🔥 Heat Index: 46.25
I (26579) DISPLAY: ┌─────────────────────────────────┐
I (26579) DISPLAY: │        SENSOR DATA DISPLAY      │
I (26579) DISPLAY: ├─────────────────────────────────┤
I (26579) DISPLAY: │ 🌡️  Temper ature:  21.10°C      │
I (26589) DISPLAY: │ 💧 Humidity:     50.30%       │
I (26589) DISPLAY: │ 🔥 Heat Index:   46.25        │
I (26589) DISPLAY: └─────────────────────────────────┘
I (26589) DISPLAY: ┌─────────────────────────────────┐
I (26589) DISPLAY: │         SYSTEM STATUS           │
I (26589) DISPLAY: ├─────────────────────────────────┤
I (26589) DISPLAY: │ Status: ✅ Comfortable         │
I (26589) DISPLAY: └─────────────────────────────────┘
I (26589) LAB7-3: ==========================================
```