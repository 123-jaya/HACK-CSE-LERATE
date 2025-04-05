🌱 Smart Irrigation System 🚀
An Arduino + Python powered irrigation assistant that makes decisions based on **crop health** (IR sensor) and **real-time weather data** — controlled wirelessly via **Bluetooth**.

Built during a 12-hour hackathon at SIT, Tumakuru (HACK-CSE-LERATE). Designed for simplicity, modularity, and future scalability 



 🔧 What It Does

- 🌦️ Fetches **weather data** based on user input (city)
- 🌿 Measures **crop health** using an IR light sensor
- ✅ Applies decision logic:
  > If crop is unhealthy OR weather is dry → irrigation needed
- 📱 Interacts with user via Bluetooth (Serial Bluetooth Terminal app)
- ⚙️ Lets user control the motor:
  - `ON 10` → Run motor for 10 seconds
  - `OFF` → Stop motor anytime
- 🛑 Automatically stops motor if **obstacle** is detected near it



 🧩 Components

| Module               | Purpose                          |
|----------------------|----------------------------------|
| Arduino Uno          | Main controller                  |
| IR Sensor (x2)       | 1 for crop, 1 for obstacle       |
| L293D Motor Driver   | Drives the motor safely          |
| HC-05 Bluetooth      | Wireless control and feedback    |
| DC Motor (Fan)       | Simulated water pump             |
| 9V Battery           | Power for the motor              |



 📱 Bluetooth User Flow

1. Enter city name (e.g., `Mumbai`)
2. App shows:
   - Weather
   - Crop health
   - Irrigation advice
3. If irrigation needed → type `ON <seconds>` (e.g., `ON 5`)
4. Motor starts, auto-stops after time or obstacle detection
5. You can also type `OFF` anytime to stop the motor


🚀 Highlights:
1. Dual IR Sensor Setup: One for monitoring crop health based on light intensity, and another for obstacle detection to ensure safety.
2. Python-Driven Weather Analysis: Real-time or simulated weather data enables smarter irrigation decisions, beyond simple sensor values.
3. Bluetooth Communication: A mobile user can interact with the system using a simple app interface, issuing commands like ON 5 or OFF to control motor behavior remotely.
4. Decision-Making Logic (OR Condition):
5. If crop health is poor OR weather suggests low humidity, the system recommends irrigation.
6. Failsafe Mechanisms:
7. Auto-stop motor on obstacle detection.
8. Timer-based motor control to avoid overwatering.
