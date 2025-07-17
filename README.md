# PowerBi____Sold-cars-from-Market


# 📊 Power BI Dashboard – Sold Cars from Market

This project is a **Power BI report** that analyzes a fictional dataset of vehicle sales. It provides interactive visuals and KPIs to help understand sales trends, inventory structure, vehicle attributes, and dealership performance.

---

## 🚗 Dataset Overview

The dataset contains detailed information about vehicles, including:

- Vehicle specifications: make, model, year, mileage, fuel type, horsepower, etc.
- Sales info: sale price, MSRP, sold/available status, sale date, dealership
- Status tracking: sold, available, in_service
- Timestamps for analysis: purchase date, sale date, created_at

---

## 📈 Key Features

- **Vehicles Sold by Month** (correctly sorted by date)
- **Total Sales Revenue**
- **Units Sold vs Available**
- **Average Sale Price**
- **Breakdown by Make, Body Type, and Engine Type**
- **Dynamic filtering by year, month, or dealership**

---

## 🧠 DAX Measures Used

```dax
Vehicles Sold = 
CALCULATE(COUNTROWS(Vehicles), Vehicles[status] = "sold")

Total Sales Revenue = 
CALCULATE(SUM(Vehicles[sale_price]), Vehicles[status] = "sold")

Average Sale Price = 
AVERAGE(Vehicles[sale_price])
