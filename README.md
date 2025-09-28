# 📌 Tasks CRUD API

A simple **Node.js + Express + MongoDB** API for managing tasks.
Supports full **CRUD operations**: Create, Read, Update, Delete.

---

## 🚀 Features

* Create a new task
* Get all tasks
* Get a task by ID
* Update an existing task
* Delete a task

---

## 📂 Project Structure

```
project/
│── app.js         # Main server file (routes + API)
│── taskModel.js   # Mongoose schema for Task
│── README.md      # Documentation
│── package.json     # package od dependencies 
```

---

## ⚙️ Installation & Setup

1. **Clone the repository**

   ```bash
   git clone <https://github.com/MennaAllahZakaria/Tasks>
   cd project
   ```

2. **Install dependencies**

   ```bash
   npm install express mongoose
   ```

3. **Run MongoDB locally**
   Make sure MongoDB is installed and running on:

   ```
   mongodb+srv://mennazakaria2003_db_user:OlCAWTNRlhwYo1MI@cluster0.lul4meu.mongodb.net/
   ```

4. **Start the server**

   ```bash
   node app.js
   ```

5. The server will run on:

   ```
   http://localhost:3000
   ```

---

## 📌 API Endpoints

### 🔹 Create Task

```http
POST /tasks
Content-Type: application/json
```

**Body Example**

```json
{
  "title": "Study Node.js",
  "description": "Finish CRUD API",
  "status": "pending"
}
```

---

### 🔹 Get All Tasks

```http
GET /tasks
```

---

### 🔹 Get Task by ID

```http
GET /tasks/:id
```

---

### 🔹 Update Task

```http
PUT /tasks/:id
Content-Type: application/json
```

**Body Example**

```json
{
  "status": "completed"
}
```

---

### 🔹 Delete Task

```http
DELETE /tasks/:id
```

---

## 📌 Example with curl

1. Create a new task:

   ```bash
   curl -X POST http://localhost:3000/tasks \
   -H "Content-Type: application/json" \
   -d '{"title":"Learn Express","description":"CRUD Example","status":"pending"}'
   ```

2. Get all tasks:

   ```bash
   curl http://localhost:3000/tasks
   ```

3. Update a task:

   ```bash
   curl -X PUT http://localhost:3000/tasks/<taskId> \
   -H "Content-Type: application/json" \
   -d '{"status":"completed"}'
   ```

4. Delete a task:

   ```bash
   curl -X DELETE http://localhost:3000/tasks/<taskId>
   ```

---

## 🛠 Tech Stack

* **Node.js**
* **Express.js**
* **MongoDB (Mongoose)**

---

## 📄 License

Free to use for learning and practice 🚀
