# Credit-Card-Complaints-Dashboard-Using-Tableau
An interactive Tableau dashboard analysing 86,893 credit card complaints  to uncover trends, hotspots, response patterns, and top issues across the US.

## 🎥 Dashboard Walkthrough
> Screen recording coming soon!

---

## 📌 Dashboard Components

| Section | Description |
|---|---|
| **Total Complaints KPI** | 86,893 total complaints tracked |
| **Timely Response KPI** | 98.90% closed on time |
| **In Progress KPI** | 329 complaints still open (0.38%) |
| **Weekly Trend** | Interactive trend chart with dynamic parameter filter |
| **State Wise Complaints** | Density map showing complaint hotspots by state |
| **Daily Complaints** | Calendar heatmap by day of the month |
| **Company Response** | Breakdown of how complaints were resolved |
| **Top Issues** | Billing disputes lead at 14,688 complaints |
| **Submitted Via** | Web dominates at 59,889 submissions |
| **Filter Panel** | Filter by number of records and date range |
| **Export Panel** | Export dashboard to PDF, image, or PowerPoint |

---

## ⚙️ Key Technical Steps

### 1. Calculated Field — Max Date Received (LOD)
```
{ MAX([Date Received]) }
```

### 2. Parameter — Max Date Received
- Created a parameter to dynamically control the rolling date window

### 3. Rolling 12 Months Filter
```
DATEDIFF('month', DATETRUNC('month', [Date Received]), 
DATETRUNC('month', [Parameters].[Max Date Received])) < 12
```

### 4. Density Map
- Built using Tableau's built-in density map feature
- Dark red areas indicate highest complaint concentration

### 5. Dynamic Trend Filter
- Parameter-driven trend toggle (Weekly/Monthly)
- Floated inside the Weekly Trend chart for a clean UI

---

## 🛠 Tools Used
- **Tableau Desktop**
- **Data Source:** CFPB Credit Card Complaints Dataset

---
