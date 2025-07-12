# 🎉 DIY Jokes API

A simple Node.js REST API built with Express.js for storing, retrieving, updating, and deleting jokes.

---

## 📂 Project Structure

.
├── index.js          # Main Express server
├── package.json
└── README.md

---

## 🚀 Features

✅ Get a random joke  
✅ Get a joke by ID  
✅ Filter jokes by type  
✅ Create a new joke  
✅ Replace or update a joke  
✅ Partially update a joke  
✅ Delete a joke  
✅ Delete all jokes (with master key)

---

## ⚙️ Installation

1️⃣ Clone the repository  
git clone <your-repo-url>  
cd <project-directory>

2️⃣ Install dependencies  
npm install

3️⃣ Run the server  
nodemon index.js  
or  
node index.js

Server will start on http://localhost:3000 (or your configured port).

---

## 🧪 API Endpoints

### 🎲 Get a random joke
GET /random  
Returns a random joke.

---

### 🔍 Get a specific joke
GET /jokes/:id  
Example: /jokes/2

---

### 🎯 Filter jokes by type
GET /filter?type=<jokeType>  
Example: /filter?type=Science

---

### ➕ Create a new joke
POST /jokes  
Body (URL-encoded):
- text=Your joke text
- type=Joke category

---

### ✏️ Replace a joke
PUT /jokes/:id  
Body (URL-encoded):
- text=Updated joke text
- type=Updated joke type

_Replaces the entire joke._

---

### 🩹 Partially update a joke
PATCH /jokes/:id  
Body (URL-encoded):
- text=New text (optional)
- type=New type (optional)

---

### 🗑️ Delete a specific joke
DELETE /jokes/:id

---

### 💣 Delete all jokes
DELETE /all?key=<masterKey>

Note: Requires the correct master key.

---

## 🔑 Master Key

The master key is defined in index.js:
const masterKey = "4VGP2DN-6EWM4SJ-N6FGRHV-Z3PR3TT";

Change this value as needed.

---

## 🧭 Example cURL Requests

✅ Create a new joke
curl -X POST http://localhost:3000/jokes \
  -d "text=This is a new joke" \
  -d "type=Funny"

✅ Delete all jokes
curl -X DELETE "http://localhost:3000/all?key=4VGP2DN-6EWM4SJ-N6FGRHV-Z3PR3TT"

✅ Get a random joke
curl http://localhost:3000/random

---

## 🛠️ Tech Stack

- Node.js
- Express
- body-parser

---

## 📝 License

This project is for educational purposes. Feel free to modify and use it as needed.
