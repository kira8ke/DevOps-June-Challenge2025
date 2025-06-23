# 🚀 Day 2: Nginx Reverse Proxy with Flask App

This project demonstrates how to set up a basic **Flask application** running behind an **Nginx reverse proxy** using **Docker Compose**. It is part of the DevOps June Challenge 2025.

---

## 📁 Project Structure

day-2-nginx-reverse-proxy/
│
├── app.py # Simple Flask application
├── Dockerfile # Dockerfile for building the Flask app image
├── docker-compose.yml # Defines services for Flask and Nginx
├── requirements.txt # Flask dependency
└── nginx/
└── nginx.conf # Nginx reverse proxy configuration

yaml
Copy
Edit

---

## 🐳 Services

- **flask-app**: Runs the Flask backend on port `5000`
- **nginx-reverse-proxy**: Listens on port `80` and proxies traffic to `flask-app`

---

## 🔧 How to Run the Project

Make sure you have Docker and Docker Compose installed.

### 1. Clone the repository:

```bash
git clone https://github.com/kira8ke/DevOps-June-Challenge2025.git
cd DevOps-June-Challenge2025/day-2-nginx-reverse-proxy
2. Build and run using Docker Compose:
bash
Copy
Edit
docker-compose up --build
3. Access the app:
Via Flask directly: http://localhost:5000

Via Nginx Reverse Proxy: http://localhost

📦 Sample Flask App Code (app.py)
python
Copy
Edit
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello():
    return 'Hello from Flask behind Nginx reverse proxy!'
📄 Nginx Config (nginx/nginx.conf)
nginx
Copy
Edit
events {}

http {
    server {
        listen 80;
        location / {
            proxy_pass http://flask-app:5000;
        }
    }
}
🧠 Concepts Covered
Dockerfile & Image creation

Flask + WSGI app containerization

Multi-service deployment with Docker Compose

Nginx reverse proxy routing

Service-to-service networking in Docker




