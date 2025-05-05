# 🎬 Movie Site - Dockerized Fullstack App

This is a fullstack Movie Site application with a **React frontend** and a **backend API** (e.g., Flask, Node.js), containerized using **Docker** and orchestrated via **Docker Compose**.

---

## 📁 Project Structure

```
Movie_Site/
│
├── frontend/             # React frontend
│   └── Dockerfile
│
├── backend/              # Backend API
│   └── Dockerfile
│
├── docker-compose.yml    # Compose file to run everything
└── README.md
```

---

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/Santhurumuthu82/Movie_Site.git
cd Movie_Site
```

### 2. Build and Run with Docker Compose

```bash
docker-compose up --build
```

This command will:

- Build the frontend and backend images
- Start both services in containers
- Map frontend to `http://localhost:3000` and backend to `http://localhost:5002`

---

## 🐳 Docker Image Management

### Build Images Manually

```bash
docker-compose build
```

### Push Images to Docker Hub

Tag and push your images after building:

```bash
docker tag movie_site_frontend yourusername/my-frontend:latest
docker tag movie_site_backend yourusername/my-backend:latest

docker push yourusername/my-frontend:latest
docker push yourusername/my-backend:latest
```

---

## ⚙️ Environment Variables

Create a `.env` file in the root if needed (for things like API keys, DB connection, etc):

```env
REACT_APP_API_URL=http://localhost:5000
BACKEND_SECRET_KEY=your_secret_key
```

Then update your Dockerfiles and app configs to use these.

---

## 🧼 Stop and Remove Containers

```bash
docker-compose down
```

To also remove volumes and images:

```bash
docker-compose down --rmi all --volumes
```

---

## 📦 Technologies Used

- 🔧 Docker & Docker Compose
- ⚛️ React (frontend)
- 🐍 Flask / Node.js (backend)
- 🐳 Nginx (optional for serving frontend)

---

## 🤝 Contributing

Feel free to fork this repo, make improvements, and submit PRs!

---

## 📄 License

This project is licensed under the MIT License.
