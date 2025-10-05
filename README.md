# ✈️ Flight Radar 2025 - Real-Time Flight Tracking Pipeline

This project simulates a **real-time flight tracking system** (similar to AirRadar 2024) using a modern data engineering pipeline.  
It generates fake flight events, streams them through Kafka, processes with Spark, stores in PostgreSQL, and visualizes with Streamlit.

---

## 🛠 Tools & Technologies

- **Python (Faker)** → Generate fake flight data (Producer)  
- **Kafka** → Message broker for real-time streaming  
- **Spark (Structured Streaming)** → Process and transform flight events  
- **Postgres** → Store flight data  
- **Streamlit** → Interactive dashboard to visualize flight positions & statuses  
- **Docker Compose** → Containerized setup for all services  

---



```
[ Python Producer (Faker) ]
            ↓
     Kafka Topic: flights
            ↓
   Spark Structured Streaming
            ↓
        PostgreSQL
            ↓
     Streamlit Dashboard
```
---

!['pipeline.png](./image/Data%20Pipeline.jpg)

## 📝 Example Data

```json
{
  "flight_id": "FL1001",
  "origin": [40.6413, -73.7781],
  "destination": [51.4700, -0.4543],
  "status": "On Time",
  "departure_time": 1695638400,
  "arrival_time": 1695645600
}
```

---

## 📌 Notes

- Kafka topic: **`flights`**  
- Postgres DB: **flights_project**  
- Streamlit UI shows flight map with status colors (On Time / Delayed / Cancelled).  
- All services are containerized and orchestrated via **Docker Compose**.

<div>
<img width="300" alt="Image" src="https://github.com/user-attachments/assets/d4c87ed2-0448-4dd4-a212-8598ae06909a" />
<img width="300" alt="Image" src="https://github.com/user-attachments/assets/28886725-02a4-4561-b1b0-06ba81efad5c" />
<img width="300" alt="Image" src="https://github.com/user-attachments/assets/65422da4-c41e-439b-b4bf-9a1f43ce7f47" />
<img width="300" alt="Image" src="https://github.com/user-attachments/assets/c4ecb565-d1ae-423b-97f7-0c1395b489bf" />
</div>

