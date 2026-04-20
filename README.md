# MongoDB-NoSQL-Assignments
A collection of MongoDB and NoSQL Assignments, queries, and practical implementations for learning database concepts.


![MongoDB Banner](https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,100:2c5364&height=220&text=MongoDB%20%7C%20NoSQL&fontSize=38&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Database%20Project&descAlignY=55&descAlign=50)

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?color=00E5FF&center=true&vCenter=true&width=500&lines=+by+Md+Ashfaque;MongoDB+%7C+NoSQL+Project;MCA+(DS+%26+AI)" />
</p>

![MongoDB Badge](https://img.shields.io/badge/Database-MongoDB-green?logo=mongodb&style=for-the-badge)
![Type Badge](https://img.shields.io/badge/Type-NoSQL-blue?style=for-the-badge)
![Status Badge](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Course Badge](https://img.shields.io/badge/Course-MCA%20(DS%20%26%20AI)-orange?style=for-the-badge)


---

👨‍🎓 Student Details

- Name: MD Ashfaque Ansari
- Course: MCA (Data Science & AI)
- Roll No: 1250259034

---
📌 Project Overview

This project demonstrates a MongoDB-based system using real-world NoSQL concepts.
It covers database creation, queries, and data analysis.

---

🔑 Key Features

- ⚡ CRUD Operations
- 📊 Aggregation Framework
- 🔗 "$lookup" Joins
- 🎯 Complex Filtering
- 🧩 Array & Subdocument Queries

---

🛠️ Tech Stack

- 🍃 MongoDB
- 💻 MongoDB Compass
- 🧠 NoSQL Concepts

---

📂 Database Collections

- 👨‍🎓 students
- 👨‍🏫 faculty
- 📘 courses
- 📝 enrollments
- 🎯 activities

---

⚙️ Setup

- Connect: "mongodb://localhost:27017"
- Database: "Mongo_Assignment"

---
## 🧪 Sample Queries

### 🎯 Students with High Attendance

```javascript id="q1x9za"
db.students.find({
  attendance: { $gt: 85 }
})
```

---

### 🔍 Students Skilled in MongoDB

```javascript id="m4k8pl"
db.students.find({
  skills: "MongoDB"
})
```

---

### 🔗 Join Students with Courses

```javascript id="8t2vsa"
db.enrollments.aggregate([
  {
    $lookup: {
      from: "courses",
      localField: "courseId",
      foreignField: "_id",
      as: "courseDetails"
    }
  }
])
```

---

### 📊 Count Students per Department

```javascript id="x7h3dn"
db.students.aggregate([
  {
    $group: {
      _id: "$department",
      totalStudents: { $sum: 1 }
    }
  }
])
```

---

### 🔄 Update Student Attendance

```javascript id="c5k2wr"
db.students.updateMany(
  { attendance: { $lt: 60 } },
  { $set: { attendance: 75 } }
)
```

---

## 📁 Project Structure

```bash id="p9v2lm"
MongoDB-Assignment/
│── README.md
│── mongo_queries.js
│── MongoDB & NOSQL Assignment Md Ashfaque.pdf
```

---

## 🎯 Learning Outcomes

* 📚 Understanding of MongoDB & NoSQL
* 📊 Writing and executing queries
* 🔗 Performing joins using $lookup
* ⚡ Data aggregation and updates


---
![MongoDB Footer](https://capsule-render.vercel.app/api?type=waving&section=footer&color=0:0f2027,100:2c5364&height=120)

