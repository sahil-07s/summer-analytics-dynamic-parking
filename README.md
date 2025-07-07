#  Dynamic Pricing for Urban Parking Lots

This project demonstrates a real-time dynamic pricing system for urban parking lots using AI/ML pipelines. The solution simulates how parking prices can adjust based on real-time parameters like occupancy, traffic, queue length, vehicle type, and special events.

Built as a capstone for **IIT Guwahati Summer Analytics 2025**.

---

##  Problem Statement

Urban parking spaces face demand fluctuations. A fixed price model often leads to either underutilization or congestion. This project aims to simulate a **dynamic pricing model** that adapts parking fees in real time, improving efficiency and user satisfaction.

---

##  Tech Stack Used

| Technology | Purpose |
|------------|---------|
| **Python 3.13** | Programming language |
| **Pandas** | Data manipulation and preprocessing |
| **NumPy** | Numeric calculations |
| **Pathway** | Real-time data streaming |
| **Bokeh** | Real-time visualization |
| **VS Code** | Development Environment |
| **Jupyter Notebook (.ipynb)** | Analysis and modeling |

---

##  How It Works

1. Load and preprocess parking lot dataset (CSV)
2. Compute real-time pricing using features:
   - Occupancy
   - Traffic conditions
   - Queue length
   - Vehicle type
   - Special events
3. Stream results with **Pathway**
4. Visualize the dynamic price live using **Bokeh**

---

##  Dynamic Pricing Formula

The price is calculated as:

```python
price = base_price + (occupancy * occupancy_weight)
              + (queue_length * queue_weight)
              + (traffic_encoded * traffic_weight)
              + (is_special_day * special_day_surcharge)
              + (vehicle_weight * vehicle_type_weight)
