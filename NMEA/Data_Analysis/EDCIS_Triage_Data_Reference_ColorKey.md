# EDCIS Triage Data Reference

## Key  
| Term | Meaning |
|------|----------|
| **PGN** | Parameter Group Number |
| **HEX** | Hexadecimal Identifier |
| **DATA TYPE** | Name of NMEA 2000 Message |
| **DESCRIPTION** | Explains what the data represents |
| **READING DATA** | How to analyze or interpret the data for anomalies |

---

## Priority Color Key
| Color | Meaning |
|--------|----------|
| 🔴 | **High Priority** |
| 🟡 | **Medium Priority** |
| 🟢 | **Low Priority** |

---

### **PGN 127237 – Heading/Track Control** 🔴
**HEX:** `0x1F105`  
**DATA TYPE:** Heading/Track Control  

**DESCRIPTION:**  
Heading track and control data is important to monitor. Data is displayed in degrees true or magnetic depending on the system when converted from hex.

**READING DATA:**  
Search for points where the heading changes abruptly or without warning. During turns, even at high speeds, heading data should still change smoothly. Compare with rudder data to confirm if heading changes align with rudder input.

---

### **PGN 127245 – Rudder** 🔴
**HEX:** `0x1F10D`  
**DATA TYPE:** Rudder  

**DESCRIPTION:**  
Rudder angle is measured in degrees. Standard rudder angle commands include 20°, 30°, and 35°, but smaller 5° adjustments are common for course corrections.

**READING DATA:**  
Look for large, sudden changes in rudder angle and note when they occur. Compare with the ordered track line to verify if a turn was commanded during any anomalies.

---

### **PGN 127250 – Vessel Heading** 🔴
**HEX:** `0x1F112`  
**DATA TYPE:** Vessel Heading  

**DESCRIPTION:**  
Indicates the ship’s direction in degrees true or magnetic.

**READING DATA:**  
Identify large or abrupt changes. Vessels can only turn at a limited rate, so compare this with rudder data to ensure consistency.

---

### **PGN 127251 – Rate of Turn** 🟡
**HEX:** `0x1F113`  
**DATA TYPE:** Rate of Turn  

**DESCRIPTION:**  
Represents how fast the vessel is turning, measured in degrees per minute.

**READING DATA:**  
Watch for rapid or unexpected changes. Keep in mind that sea state and weather can affect readings.

---

### **PGN 127258 – Magnetic Variation** 🟢
**HEX:** `0x1F11A`  
**DATA TYPE:** Magnetic Variation  

**DESCRIPTION:**  
Shows the difference between true north and magnetic north, expressed in degrees.

**READING DATA:**  
The vessel’s gyro that measures true north cannot be hacked, but variations should still be noted.

---

### **PGN 127488 – Engine Parameters, Rapid Update** 🟢
**HEX:** `0x1F200`  
**DATA TYPE:** Engine Parameters, Rapid Update  

**DESCRIPTION:**  
n/a  

**READING DATA:**  
n/a  

---

### **PGN 128259 – Speed, Water Referenced** 🟡
**HEX:** `0x1F503`  
**DATA TYPE:** Speed, Water Referenced  

**DESCRIPTION:**  
n/a  

**READING DATA:**  
n/a  

---

### **PGN 128267 – Water Depth** 🟡
**HEX:** `0x1F50B`  
**DATA TYPE:** Water Depth  

**DESCRIPTION:**  
Displays current water depth in feet.

**READING DATA:**  
Watch for drastic or unrealistic depth changes, especially those deviating more than 10 feet from charted depth.

---

### **PGN 128275 – Distance Log** 🟢
**HEX:** `0x1F513`  
**DATA TYPE:** Distance Log  

**DESCRIPTION:**  
Displays total distance traveled in nautical miles.

**READING DATA:**  
Check for anomalies in distance changes or unexpected resets.

---

### **PGN 129025 – Position, Rapid Update** 🔴
**HEX:** `0x1F801`  
**DATA TYPE:** Position, Rapid Update  

**DESCRIPTION:**  
Provides vessel position in latitude and longitude.

**READING DATA:**  
Look for sudden, inconsistent position changes.

---

### **PGN 129026 – COG & SOG, Rapid Update** 🟡
**HEX:** `0x1F802`  
**DATA TYPE:** Course Over Ground & Speed Over Ground  

**DESCRIPTION:**  
Shows COG in degrees and SOG in knots.

**READING DATA:**  
Identify large or repeated changes over multiple readings.

---

### **PGN 129029 – GNSS Position Data** 🔴
**HEX:** `0x1F805`  
**DATA TYPE:** GNSS Position Data  

**DESCRIPTION:**  
Displays the vessel’s digital position on charts and radar.

**READING DATA:**  
Look for consistent data shifts. Compare with rudder to confirm if changes reflect actual movement.

---

### **PGN 129033 – Local Time Offset** 🟢
**HEX:** `0x1F809`  
**DATA TYPE:** Local Time Offset  

**DESCRIPTION:**  
Displays local vessel time.

**READING DATA:**  
Not typically a target for manipulation.

---

### **PGN 129044 – Datum** 🟢
**HEX:** `0x1F814`  
**DATA TYPE:** Datum  

**DESCRIPTION:**  
n/a  

**READING DATA:**  
n/a  

---

### **PGN 129283 – Cross Track Error** 🟡
**HEX:** `0x1F903`  
**DATA TYPE:** Cross Track Error  

**DESCRIPTION:**  
Indicates deviation from the plotted course in yards.

**READING DATA:**  
Compare vessel’s actual position with the plotted course to confirm if cross-track error is accurate.

---

### **PGN 129284 – Navigation Data** 🟢
**HEX:** `0x1F904`  
**DATA TYPE:** Navigation Data  

**DESCRIPTION:**  
n/a  

**READING DATA:**  
n/a  
