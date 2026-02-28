# AI Smart Meeting Scheduler

## 📌 Project Overview

AI Smart Meeting Scheduler is a rule-based web application built using FastAPI.  
It helps in automatically generating and ranking meeting time slots based on participant availability and time preference.

This is a local demo project that simulates scheduling logic without integrating Google Calendar or sending real emails.

---

## 🎯 Problem Statement

Manually finding a common meeting time for multiple participants can be difficult and time-consuming.

This project solves that problem by:
- Comparing availability of multiple participants
- Ranking time slots intelligently
- Preventing double booking of meetings

---

## ⚙️ How The System Works

1. The system creates predefined time slots for the next 3 days.
2. Three participants are simulated:
   - Alice
   - Bob
   - Charlie
3. For each time slot, the system checks how many participants are available.
4. Each slot is assigned a score using this formula:

   Score = Number of available participants  
   + 2 bonus points if the time is before 12 PM

5. Slots are sorted by:
   - Date
   - Highest score first

6. If a meeting is booked:
   - That slot is removed from available options.
   - A simulated email confirmation is printed in the terminal.

---

## ✨ Features Implemented

- Simple login system (simulated session-based authentication)
- Multi-participant availability comparison
- Intelligent slot ranking using scoring logic
- Morning time preference bonus
- Conflict detection (prevents double booking)
- Meeting booking system
- Simulated email notification (console print)
- Clean user interface using HTML and CSS

---

## 🛠️ Technologies Used

Backend:
- Python
- FastAPI

Frontend:
- HTML
- CSS
- Jinja Templates

Server:
- Uvicorn

---

## 📂 Project Structure

- main.py → Backend logic and smart scheduling engine  
- templates/ → HTML pages (index.html, login.html)  
- static/ → CSS styling  
- requirements.txt → Project dependencies  
- README.md → Project documentation  

---

## ▶️ How To Run The Project

1. Install dependencies:

python -m pip install -r requirements.txt

2. Run the server:

python -m uvicorn main:app --reload

3. Open in browser:

http://127.0.0.1:8000

---

## 🧠 Smart Logic Explanation (Core Part)

The main intelligent function is `generate_smart_slots()`.

It:
- Counts how many participants are free in each slot
- Adds bonus score for morning slots
- Removes already booked slots
- Sorts slots by date and priority score

This rule-based scoring system simulates AI-style decision-making without using machine learning.

---

## ⚠️ Important Note

This project does NOT connect to:
- Google Calendar API
- Gmail API

Meeting bookings and email confirmations are simulated locally to demonstrate scheduling logic.

---

## 🚀 Challenges Faced

- Designing a logical scoring system
- Managing session state without a database
- Preventing duplicate meeting bookings
- Dynamically updating available slots after booking

---

## 🔮 Future Improvements

- Integration with Google Calendar API
- Real email notifications
- Database storage (MongoDB)
- Deployment on cloud platform

---

## 👩‍💻 Author

Hiba Saeed
