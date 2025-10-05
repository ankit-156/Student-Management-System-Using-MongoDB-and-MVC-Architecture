# 🎓 Student Management API (Express + MongoDB)

A simple RESTful API for managing **students** using **Node.js**, **Express**, and **MongoDB (Mongoose)**.

---

## ✨ Features
- ➕ Add a new student  
- 📖 View all students  
- 🔍 Get student by ID  
- ✏️ Update student details  
- 🗑️ Delete student record  

---

## 🛠 Tech Stack
- [Node.js](https://nodejs.org/)  
- [Express](https://expressjs.com/)  
- [MongoDB](https://www.mongodb.com/)  
- [Mongoose](https://mongoosejs.com/)  
- [CORS](https://www.npmjs.com/package/cors)  

---

## ⚙️ Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/your-username/student-management.git
cd student-management
```

### 2. Install dependencies
```bash
npm install
```

### 3. Start MongoDB server
Ensure MongoDB is running locally at:
```
mongodb://127.0.0.1:27017/studentDB
```

Example (Linux/macOS):
```bash
mongod
```

### 4. Run the server
```bash
node index.js
```

Or with nodemon (auto-restart):
```bash
npx nodemon index.js
```

### 5. Server will be available at
```
http://localhost:3000
```

---

## 📌 API Endpoints

### 1. ➕ Create Student
**POST** `/students`

**Body (JSON):**
```json
{
  "name": "John Doe",
  "age": 22,
  "course": "Computer Science"
}
```

**Response (201 Created):**
```json
{
  "_id": "64f9a1b2e3a4c5d6f7a8b901",
  "name": "John Doe",
  "age": 22,
  "course": "Computer Science",
  "__v": 0
}
```

---

### 2. 📖 Get All Students
**GET** `/students`

**Response (200 OK):**
```json
[
  {
    "_id": "64f9a1b2e3a4c5d6f7a8b901",
    "name": "John Doe",
    "age": 22,
    "course": "Computer Science"
  },
  {
    "_id": "64f9a1b2e3a4c5d6f7a8b902",
    "name": "Jane Smith",
    "age": 21,
    "course": "Mathematics"
  }
]
```

---

### 3. 🔍 Get Student by ID
**GET** `/students/:id`

**Response (200 OK):**
```json
{
  "_id": "64f9a1b2e3a4c5d6f7a8b901",
  "name": "John Doe",
  "age": 22,
  "course": "Computer Science"
}
```

---

### 4. ✏️ Update Student by ID
**PUT** `/students/:id`

**Body (JSON):**
```json
{
  "name": "John Doe",
  "age": 23,
  "course": "Data Science"
}
```

**Response (200 OK):**
```json
{
  "_id": "64f9a1b2e3a4c5d6f7a8b901",
  "name": "John Doe",
  "age": 23,
  "course": "Data Science"
}
```

---

### 5. 🗑️ Delete Student by ID
**DELETE** `/students/:id`

**Response (200 OK):**
```json
{
  "message": "Student deleted successfully",
  "student": {
    "_id": "64f9a1b2e3a4c5d6f7a8b901",
    "name": "John Doe",
    "age": 23,
    "course": "Data Science"
  }
}
```

---

## 🧪 Testing with Postman

1. Open **Postman** and set the base URL:  
   ```
   http://localhost:3000/students
   ```

2. Available requests:
   - `POST /students` → Add student  
   - `GET /students` → Get all students  
   - `GET /students/:id` → Get student by ID  
   - `PUT /students/:id` → Update student  
   - `DELETE /students/:id` → Delete student  

3. Set request **Body → raw → JSON** for POST/PUT requests.  
4. For GET/PUT/DELETE by ID, use the `_id` value from POST response.  

---

## 🧰 Troubleshooting
- **MongoDB connection error** → Make sure `mongod` is running.  
- **CastError (ObjectId)** → Invalid MongoDB `_id`.  
- **Validation error** → Ensure all required fields (`name`, `age`, `course`) are provided.

## 🖼️ OUTPUT

![Output 1](./OUTPUT/Screenshot%202025-10-05%20225407.png)
![Output 2](./OUTPUT/Screenshot%202025-10-05%20225619.png)
![Output 3](./OUTPUT/Screenshot%202025-10-05%20225704.png)
![Output 4](./OUTPUT/Screenshot%202025-10-05%20225758.png)





