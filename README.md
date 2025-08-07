# Interactive-EV-vehicle-registration-dashboard
A Streamlit Dashboard to visualize Quarterly and Yearly Growth in Ev -vehicle registration using interactive charts
# 📊 Interactive EV Vehicle Registration Dashboard

This is a Streamlit-based interactive dashboard that visualizes electric vehicle (EV) registration trends across manufacturers and vehicle types in India. The dashboard allows investors and analysts to track quarterly growth (QoQ, YoY) using real-world data.

##  Features

-  Line and bar charts for registration trends
-  QoQ and YoY growth analysis
-  Manufacturer & Vehicle-type filters
-  Dynamic quarter range selection
-  KPI metrics for total registrations & latest quarter

## 🗃 Dataset

The data is taken from the *Ministry of Road Transport's Vahan Dashboard* and includes:

- Manufacturer name
- Vehicle type (2W, 3W, 4W)
- Registration date
- Number of units registered
- Quarter
- QoQ Growth
- YoY Growth

##  How to Run

1. Clone the repo:
    ```bash
    git clone https://github.com/your-username/interactive-ev-vehicle-registration-dashboard.git
    cd interactive-ev-vehicle-registration-dashboard
    ```

2. Install the requirements:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the app:
    ```bash
    streamlit run app.py
    ```

##  Requirements

- Python 3.8+
- Streamlit
- Pandas
- Plotly (if using charts)



---

> Created by Abhishek Kumar
