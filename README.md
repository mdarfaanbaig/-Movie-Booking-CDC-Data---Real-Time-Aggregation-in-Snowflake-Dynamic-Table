# -Movie-Booking-CDC-Data---Real-Time-Aggregation-in-Snowflake-Dynamic-Table

🚀 A real-time movie booking dashboard that aggregates data from CDC (Change Data Capture) sources using Snowflake Dynamic Tables and visualizes it in an interactive Streamlit web application.

📌 Features

✅ Real-time CDC Data Processing – Leverages Snowflake Dynamic Tables to handle streaming updates.

✅ Interactive Streamlit Dashboard – Provides insights on bookings, revenue, and ticket sales.

✅ Custom Filters – Users can filter data by date range and booking status.

✅ Data Aggregation & Visualization – Uses Snowflake Snowpark for data transformation and Altair/Matplotlib for charts.


Tech Stack : Python, Snowflake Dynamic Table, Snowflake Stream, Snowflake Tasks, Streamlit

-> Create Snowflake table which will keep raw movies booking data
-> Setup stream on raw table
-> Create snowflake table (Bronze layer) to keep raw data along with cdc metadata information
-> Schedule task to ingest incremental data from stream to bronze table every 1 minute
-> Create dynamic table (Silver layer) to keep filtered data from bronze table
-> Create dynamic table (Gold layer) with aggregation logic on top of silver table
-> Schedule task to refresh gold table every 2 minutes
-> Create streamlit application in snowflake for real time dashboard using snowpark library
