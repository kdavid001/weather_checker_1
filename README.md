# weather_checker_1
## ☁️ Rain Alert Script with OpenWeatherMap and Twilio

This Python script checks the weather forecast using the OpenWeatherMap API and sends you an SMS alert via Twilio if it's expected to rain.

---

## 📌 Features
- ⛅ Uses OpenWeatherMap's 5-day/3-hour forecast API.
- 📲 Sends SMS notification through Twilio if rain is detected.
- 🕒 Can be scheduled to run daily (e.g., using Task Scheduler or Cron).

---

## 🛠 Requirements

- Python 3.x
- `requests` library
- `twilio` library

Install the required libraries with:

```bash
pip install requests twilio
```


⸻

🔐 API Keys Required

You’ll need the following to get started:

	• 🌦 A OpenWeatherMap API Key: https://openweathermap.org/api
	• 📞 A Twilio Account SID and Auth Token: https://www.twilio.com/
 
Replace the placeholders in rain_alert.py:

```
api_key = "__YOUR_OWM_API_KEY__"
account_sid = "__YOUR_TWILIO_ACCOUNT_ID__"
auth_token = "__YOUR_TWILIO_AUTH_TOKEN__"
```
Also update the phone numbers:
```
from_="YOUR TWILIO VIRTUAL NUMBER"
to="YOUR TWILIO VERIFIED REAL NUMBER"
```

⸻

📍 Weather Location

Currently configured for:

Covenant University
Latitude: 46.947975
Longitude: 7.447447

(You can update these values in the weather_params dictionary.)

⸻

⚙️ How It Works
	1.	Sends a request to OpenWeatherMap for the weather forecast.
	2.	Parses the data for upcoming 3-hour weather conditions.
	3.	If rain is detected (weather condition code < 700), it sends you a reminder SMS using Twilio.

⸻

▶️ Running the Script

Once set up, run the script using:
```
python rain_alert.py
```

📝 Notes
	•	Twilio trial accounts only support verified phone numbers.
	•	Make sure your Twilio account is funded or upgraded for full access.
	•	You can tweak the message or notification time based on your preference.
