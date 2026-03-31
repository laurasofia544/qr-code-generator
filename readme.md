# QR Code Generator (Dockerized)

## Project Overview
This project is a Dockerized QR Code Generator built using Python. It generates QR codes based on a given URL and saves them as image files. The application is containerized using Docker so it can run consistently across different environments.

## Repository Contents
This repository includes:
- `main.py` — the main Python application
- `requirements.txt` — Python dependencies
- `Dockerfile` — Docker build instructions
- `docker-compose.yml` — Docker Compose configuration
- `.github/workflows/docker.yml` — GitHub Actions workflow for Docker build
- `screenshots/` — screenshots for submission

## How to Run

### Run Locally
```bash
python main.py
```
### Run with Docker
```
docker build -t qr-code-generator-app .
docker run -d --name qr-generator qr-code-generator-app
docker logs qr-generator
```
### Stop and Remove the Container
```
docker build -t qr-code-generator-app .
docker run -d --name qr-generator qr-code-generator-app
docker logs qr-generator
```
### Docker Image
<img width="1919" height="1066" alt="Screenshot 2026-03-30 203117" src="https://github.com/user-attachments/assets/5e86a464-39d9-431b-8775-ca59b3042dd2" />

## Screenshots
### Docker Logs
<img width="1173" height="116" alt="docker-logs" src="https://github.com/user-attachments/assets/de427816-8e3d-4a37-906a-d3c541cf640e" />
### Github Actions
<img width="1900" height="1068" alt="github-actions" src="https://github.com/user-attachments/assets/96668e08-bafd-4daa-82f0-b0c273408f68" />

## Reflection
For this assignment, I Dockerized a QR Code Generator application and uploaded it to GitHub and DockerHub. One of the biggest challenges I faced when completing the project was installing the project dependencies. At first, the installation failed because I was using Python 3.13, which caused compatibility issues with the Pillow library listed in the requirements file. I fixed this by installing Python 3.12 and creating a new virtual environment, which allowed the dependencies to install correctly.

Another challenge I ran into was getting Docker Desktop to start properly. At first, Docker would not run, so my Docker build command failed even though the Dockerfile itself was correct. After restarting Docker Desktop and trying again, I was able to successfully build the Docker image and run the container.

This project helped me better understand how Docker can package an application with all of its dependencies, and how GitHub and DockerHub can be used together to share and manage a project. It also showed me how important version compatibility is when working with Python packages.
