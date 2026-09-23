# Logistics Operations & Fleet Performance Analytics

An interactive Power BI dashboard designed to analyze logistics operations, fleet performance, customer revenue, driver productivity, delivery performance, operational costs, and safety.

The project demonstrates the use of **Power Query, data modeling, DAX, time intelligence, KPI development, and interactive dashboard design** to transform relational logistics data into actionable business insights.

---

## Project Overview

Logistics companies generate large amounts of operational data across customers, loads, trips, vehicles, drivers, fuel purchases, maintenance activities, delivery events, and safety incidents.

The objective of this project was to build a centralized analytical solution that answers:

- How is the logistics operation performing overall?
- Which customers contribute the most revenue?
- How efficiently is the fleet being utilized?
- How are drivers performing?
- Which routes, loads, and freight types contribute to revenue?
- What are the major operational costs?
- Where are delivery and safety issues occurring?

The final solution is a **4-page interactive Power BI dashboard**.

---

## Business Objectives

The analysis focuses on six major areas:

### 1. Revenue & Financial Performance
- Analyze total revenue
- Measure revenue by customer
- Analyze revenue by freight type
- Compare revenue against operational costs
- Track revenue trends over time
- Calculate revenue per mile

### 2. Customer Performance
- Identify high-value customers
- Analyze revenue by customer type
- Compare current customer earnings with annual revenue potential
- Analyze customer loads and booking types

### 3. Fleet Performance
- Measure fleet utilization
- Analyze miles travelled
- Analyze fleet revenue
- Compare MPG across fleet assets
- Identify downtime
- Compare fleet performance by vehicle make

### 4. Driver Performance
- Analyze driver revenue
- Track trips completed
- Measure miles travelled
- Analyze driver MPG
- Measure on-time delivery performance
- Monitor idle hours

### 5. Delivery & Operational Performance
- Analyze on-time delivery
- Measure detention time
- Analyze loads by freight type
- Examine revenue by origin and destination
- Compare route performance

### 6. Cost, Maintenance & Safety
- Analyze fuel expenditure
- Calculate fuel cost per mile
- Analyze maintenance expenditure
- Track maintenance events
- Analyze safety incidents
- Measure vehicle and cargo damage costs
- Track claims

---

# Dataset

The project uses a relational logistics dataset consisting of **14 CSV tables**.

### Core Tables

| Table | Purpose |
|---|---|
| Customers | Customer information and account characteristics |
| Loads | Shipment and revenue information |
| Routes | Origin, destination and route characteristics |
| Trips | Trip execution and vehicle/driver assignments |
| Drivers | Driver information and employment details |
| Trucks | Fleet vehicle information |
| Trailers | Trailer inventory |
| Fuel Purchases | Fuel transactions and costs |
| Maintenance Records | Vehicle maintenance activities and costs |
| Delivery Events | Pickup/delivery events and delivery performance |
| Safety Incidents | Operational incidents and claims |
| Facilities | Facility and terminal information |
| Driver Monthly Metrics | Monthly driver performance |
| Truck Utilization Metrics | Monthly fleet utilization |

---

# Data Preparation

The data was prepared using **Power Query** before being loaded into the Power BI data model.

### Data preparation activities included:

- Data type validation
- Column formatting
- Missing-value inspection
- Duplicate validation
- Key validation
- Relationship validation
- Foreign-key inspection
- Date formatting
- Dataset consistency checks

Missing foreign keys in operational fact tables were retained rather than artificially assigning IDs, ensuring that the analysis did not fabricate operational records.

---

# Data Model

A relational model was created connecting operational fact tables with their corresponding dimension tables.

Key relationships include:

```text
Customers
    │
    └── Loads
          │
          └── Trips
                ├── Fuel Purchases
                ├── Delivery Events
                └── Safety Incidents

Drivers ─────────── Trips

Trucks ──────────── Trips
   │
   └── Maintenance Records.
```
A dedicated DimDate table was also created to support time-based analysis and Year-over-Year calculations.
More than 49 DAX measures were created to support the dashboard.

Dashboard Pages
1. Executive Overview

Provides a high-level view of the organization's operational and financial performance.

<img width="578" height="330" alt="Executive Overview" src="https://github.com/user-attachments/assets/f5d83fb9-5324-4f3f-bc25-90289dc153dc" />

2. Customer Analytics

Focuses on customer contribution and revenue opportunities.

<img width="578" height="326" alt="Customer Anal" src="https://github.com/user-attachments/assets/84d1eb5d-4dee-4246-af3b-304c2460133b" />


3. Fleet Stats

<img width="578" height="327" alt="Fleet Anal" src="https://github.com/user-attachments/assets/89f603d5-3d88-45bb-b20e-411c8b215403" />

Analyzes fleet productivity and asset utilization.

4. Driver Performance

Analyzes driver productivity, efficiency, and delivery performance.

<img width="578" height="328" alt="Driver" src="https://github.com/user-attachments/assets/e0bda643-facb-4a2b-bd81-de880f96f953" />


# Key KPIs

The dashboard incorporates operational and financial KPIs including:

KPI	Purpose
Total Revenue	Measures overall revenue generated
Total Loads	Measures shipment volume
Total Trips	Measures transportation activity
Fleet Utilization	Measures how effectively fleet assets are being used
Revenue per Mile	Measures revenue generated per mile
Fuel Cost per Mile	Measures fuel efficiency from a cost perspective
On-Time Delivery Rate	Measures delivery reliability
Average MPG	Measures fuel efficiency
Fleet Downtime	Measures unavailable fleet capacity
Maintenance Cost	Measures vehicle maintenance expenditure
Safety Incidents	Measures operational incidents
Claims	Measures financial exposure from incidents

 # Business Insights

The dashboard provides a framework for identifying:

High-value customers and customer segments
Fleet assets generating significant revenue
Differences in vehicle utilization
Fuel cost patterns
Maintenance-intensive vehicles
Driver productivity differences
Delivery reliability issues
Revenue concentration by freight type
Operational cost trends
Areas where additional investigation may be required

The dashboard is designed to allow users to move from high-level KPIs to detailed operational analysis using slicers and cross-filtering.

# Tools & Technologies
Microsoft Power BI
Power Query
DAX
Microsoft Excel
Relational Data Modeling
Data Cleaning & Transformation
Time Intelligence
Data Visualization

Created by
Stephen Emesiana
Data Analyst 

