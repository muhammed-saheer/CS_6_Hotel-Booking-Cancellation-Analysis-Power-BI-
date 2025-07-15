# 🏨 Hotel Booking Cancellation Analysis (Power BI)

This project analyzes real-world hotel booking data to uncover insights about cancellations, seasonal pricing, guest behaviors, and booking patterns. The analysis is based on data from two hotels (Resort and City) collected from **2015 to 2017**.

---

## 📂 Dataset Info

- **Source**: [ScienceDirect – Hotel Booking Demand Dataset](https://www.kaggle.com/jessemostipak/hotel-booking-demand)
- **File Used**: `hotel_bookings.csv`
- **Size**: 119,390 records
- **Variables**: Lead time, cancellation status, deposit type, market segment, pricing (ADR), guest types, etc.

---

## 🔍 Business Questions & Analysis

### 🎯 Q1: What is the relationship between lead time and cancellation?

- **Goal**: Determine if customers who book earlier (longer lead time) cancel more.
- **Steps**:
  - Created a column `LeadTime_Bin` to group bookings
  - Used a stacked column chart: `LeadTime_Bin` on X-axis, Count of `IsCanceled` on Y-axis
- **Observation**: Longer lead time bookings have a higher cancellation rate.
- **Conclusion**: Guests who book early are more likely to cancel. Hotels should consider stricter policies for long lead time bookings.

📸 ![Q1](https://github.com/muhammed-saheer/CS_6_Hotel-Booking-Cancellation-Analysis-Power-BI-/blob/main/images/Lead%20Time%20Impact.png)

---

### 💰 Q2: What is the relationship between deposit type and cancellation?

- **Goal**: Understand how deposits affect cancellations.
- **Steps**:
  - Plotted `DepositType` vs. `IsCanceled` using a 100% stacked bar chart
- **Observation**: Most cancellations are from bookings with **No Deposit**. Bookings with **Non Refund** deposits rarely cancel.
- **Conclusion**: Requiring a deposit, especially non-refundable, helps reduce cancellations.

📸 ![Q2](https://github.com/muhammed-saheer/CS_6_Hotel-Booking-Cancellation-Analysis-Power-BI-/blob/main/images/Deposit%20Policy%20Effect.png)

---

### 🧑‍💼 Q3: What is the relationship between market segment and cancellation?

- **Goal**: Identify which market segments cancel more often.
- **Steps**:
  - Used `MarketSegment` on X-axis and Count of `IsCanceled` on Y-axis
- **Observation**: **Online TA** and **Groups** cancel more than Corporate or Direct bookings.
- **Conclusion**: Focus on retaining corporate/direct customers and apply cancellation buffers for OTA/group bookings.

📸 ![Q3](https://github.com/muhammed-saheer/CS_6_Hotel-Booking-Cancellation-Analysis-Power-BI-/blob/main/images/Market%20Segment%20Insights.png)

---

### 🔁 Q4: What is the relationship between previous cancellations and current cancellations?

- **Goal**: Do guests who canceled before cancel again?
- **Steps**:
  - Bar chart of `PreviousCancellations` vs Count of `IsCanceled`
- **Observation**: Guests with previous cancellations are much more likely to cancel again.
- **Conclusion**: Hotels should flag repeat cancelers and apply stricter policies or deposit requirements.

📸 ![Q4](https://github.com/muhammed-saheer/CS_6_Hotel-Booking-Cancellation-Analysis-Power-BI-/blob/main/images/Repeat%20Cancellers%20Behavior.png)

---

### 📅 Q5: How much does the price in hotels vary over the year?

- **Goal**: Analyze seasonal pricing trends.
- **Steps**:
  - Combined `ArrivalDateYear` and `ArrivalDateMonth` to build `Arrival Date`
  - Line chart: `Arrival Date` vs Average `ADR` (filtered ADR > 0)
- **Observation**: Prices rise in summer (June–August) and December.
- **Conclusion**: Hotel pricing is seasonal. Revenue can be optimized by adjusting rates during high-demand periods.

📸 ![Q5](https://github.com/muhammed-saheer/CS_6_Hotel-Booking-Cancellation-Analysis-Power-BI-/blob/main/images/Seasonal%20Pricing%20Analysis.png)

---

## 📊 Power BI Dashboard

- 📁 File: `Hotel_Booking_Cancellation_Analysis.pbix`
- 📌 Pages:
  1. **Lead Time Impact**
  2. **Deposit Policy Effect**
  3. **Market Segment Insights**
  4. **Repeat Cancellers Behavior**
  5. **Seasonal Pricing Analysis**

---

## 👨‍💻 Author

**Muhammed Saheer K**  
[🔗 Portfolio Website](https://muhammed-saheer.github.io/muhammedsaheer.github.io/)  
[🔗 LinkedIn](https://www.linkedin.com/in/muhammed-saheer-k-34a7372a8/)  
[🔗 GitHub](https://github.com/muhammed-saheer)
