# Uber_PBI_Dashboard




# 🚗 Uber Ride Analysis Dashboard  
**📅 Dataset**: Uber Trip Logs – NYC (June 2024)  
**🔧 Tool Used**: Power BI Desktop

## 📌 Overview  
This dashboard presents a deep-dive into New York City Uber trips using transactional-level ride data. It analyzes patterns in bookings, trip distances, payment behavior, vehicle types, and location-based insights—crafted for technical audiences and open-source portfolio sharing.

---

## ⚙️ Technical Design  

- **Modeling Approach**:  
  - Star schema with a centralized fact table (`Trips`)  
  - Dimension tables for `VehicleType`, `PaymentType`, `Location`, and `DateTime`  

- **Power Query**:  
  - Location normalization, time column parsing, and creation of time bins  

- **DAX Measures**:
  ```DAX
  Total Booking Value = SUM('Trips'[Booking Value])  
  Avg Fare = AVERAGE('Trips'[Booking Value])  
  Trip Distance Bucket = SWITCH(...)
  ```

- **Time Intelligence**:  
  - Day/Night classification using pickup hour logic  
  - Visual segmentation by weekday and hour-of-day  

---

## 🔢 Key Metrics  

| Metric               | Value      |
|----------------------|------------|
| Total Bookings       | 103,728    |
| Total Booking Value  | $1.6M      |
| Average Distance     | 3 miles    |
| Average Duration     | 16 minutes |
| Total Trip Distance  | 349K miles |
| Avg Fare per Trip    | $15        |

---

## 🔍 Analytical Layers  

### 🕒 Time Analysis  
- Ride volumes peak between 9 AM–6 PM  
- Highest bookings on Mondays and Tuesdays  
- ~65% of trips classified as “Day Trips”

### 🚗 Vehicle Type Distribution  
- UberX is the most preferred vehicle across pickup zones  
- Average fare remains consistent across all vehicle types

### 💳 Payment Breakdown  
- Uber Pay: ~67% of all transactions  
- Secondary methods: Cash, Google Pay, Amazon Pay

### 📍 Location Intelligence  
- Most frequent pickup: Penn Station / Madison Sq  
- Top drop-off: Upper East Side North  
- Farthest ride: Lower East Side → Crown Heights North

---

## 💼 Project Value  
This dashboard demonstrates:
- Real-world application of Power BI modeling and visualization  
- Advanced DAX and Power Query transformations for structured insight  
- Context-aware analytics useful for urban mobility, pricing analysis, and operational planning




