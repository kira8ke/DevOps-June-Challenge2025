# 🚀 Day 1 - Flask Docker App

This is the first challenge in my **DevOps June Challenge 2025**. Today’s goal was to build and containerize a simple Flask application using Docker.

---

## ✅ What Was Achieved

- Created a basic **Flask app** (`app.py`) that returns a simple "Hello from Flask!" response.
- Added a `requirements.txt` file to manage Python dependencies.
- Wrote a **Dockerfile** to containerize the app.
- Built the Docker image:
  ```bash
  docker build -t flask-docker-app .
-Ran the containerized app:
docker run -d -p 5000:5000 flask-docker-app
-Accessed the running app via http://localhost:5000.
-Created a structured folder for Day 1 with its own README.md.
-Successfully pushed the project to GitHub: DevOps-June-Challenge2025

🛠️ Technologies Used
Python 3
Flask
Docker
Git & GitHub

⚠️ Challenges Faced & Fixed
❌ Docker daemon not running → ✅ Launched Docker Desktop to fix.

❌ Dockerfile was empty → ✅ Rewrote and added the correct build steps.

❌ Container exited immediately → ✅ Checked logs, fixed app errors.

❌ Git push rejected → ✅ Resolved using git pull --rebase and then git push.

🧠 What I Learned
1)How to write and structure a basic Dockerfile.
2)How to containerize a Flask app and run it using Docker.
3)Troubleshooting container issues using docker logs and docker ps.
4)How to use Git effectively to sync local and remote repositories.
5)How to organize DevOps projects for clarity and scalability.





