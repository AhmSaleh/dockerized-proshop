# ProShop eCommerce Platform

This eCommerce platform is built using the MERN stack (MongoDB, Express, React, Node.js) with Redux for state management.

## Usage

### Building Docker Images

To build the Docker images for the frontend and backend, follow these steps:

1. **Frontend Image:**
   - Navigate to the `frontend` directory.
   - Run the following command to build the frontend image:
     ```bash
     docker build -t frontend .
     ```

2. **Backend Image:**
   - Navigate to the `backend` directory.
   - Run the following command to build the backend image:
     ```bash
     docker build -t backend .
     ```

### Running Containers

Before running the containers, you should create a Docker network to enable communication between the frontend and backend containers:

```bash
docker network create my_network
```

Now, you can run the backend and frontend containers using the created network:

```bash
docker run -it -p 5000:5000 --name backend --network my_network backend
```
```bash
docker run -it -p 3000:3000 --network my_network frontend
```

### Sample User Logins

```
admin@example.com (Admin)
123456

john@example.com (Customer)
123456

jane@example.com (Customer)
123456
```