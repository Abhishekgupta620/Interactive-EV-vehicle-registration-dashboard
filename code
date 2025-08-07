import pandas as pd
import streamlit as st

def parse_quarter(qstr):
    try:
        year = qstr[:4]
        q = qstr[-2:]
        month_map = {'Q1': '01', 'Q2': '04', 'Q3': '07', 'Q4': '10'}
        if q in month_map:
            return pd.to_datetime(f"{year}-{month_map[q]}-01")
    except:
        return pd.NaT

# Load the data
df = pd.read_csv("vehicle_data_sample.csv")
df.columns = ["Company", "Vehicle", "Date", "Units", "Quarter", "QoQ_Growth", "YoY_Growth"]
df['quarter'] = df['Quarter'].apply(parse_quarter)
df = df.dropna(subset=['quarter'])

# Streamlit UI
st.title("📊 EV Market Analysis Dashboard")
st.markdown("Analyze growth of 2W, 3W, 4W vehicles from leading EV companies 🚗⚡")

# Filter section
company_options = df["Company"].unique()
vehicle_options = df["Vehicle"].unique()

selected_company = st.selectbox("Select Company", company_options)
selected_vehicle = st.selectbox("Select Vehicle Type", vehicle_options)

# Filtered DataFrame
filtered_df = df[
    (df["Company"] == selected_company) &
    (df["Vehicle"] == selected_vehicle)
]

st.subheader(f"📈 Data for {selected_company} - {selected_vehicle}")
st.dataframe(filtered_df)
