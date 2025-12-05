# Student-management-mongodb
# 📚 Student Management System (MongoDB)

A simple and clean **Student Management System** built using **MongoDB**.  
This project focuses on database design, CRUD operations, relationships, and basic aggregation lookup.  
Perfect for learning database concepts and showcasing in interviews.

---

## 🚀 Features

- Add, update, delete and view students  
- Store teacher details  
- Add courses and enroll students  
- Maintain marks for each course  
- Track student attendance  
- Demonstrates relationships using ObjectId  
- Includes `$lookup` for joining collections

---

## 🗂️ Collections Overview

### **1. Students**
| Field | Description |
|-------|-------------|
| studentId (ObjectId) | Primary Key |
| name | Student name |
| class | Class/Section |
| rollno | Roll Number |
| phone | Contact number |

### **2. Teachers**
| Field | Description |
|-------|-------------|
| teacherId (ObjectId) | Primary Key |
| name | Teacher name |
| subject | Subject taught |
| phone | Contact number |

### **3. Courses**
| Field | Description |
|-------|-------------|
| courseId (ObjectId) | Primary Key |
| courseName | Course Name |
| class | Class related to course |

### **4. Enrollments**
| Field | Description |
|-------|-------------|
| enrollmentId (ObjectId) | Primary Key |
| studentId (FK) | Ref → Students |
| courseId (FK) | Ref → Courses |
| enrollmentDate | Date |

### **5. Marks**
| Field | Description |
|-------|-------------|
| markId (ObjectId) | Primary Key |
| studentId (FK) | Ref → Students |
| courseId (FK) | Ref → Courses |
| marks | Marks obtained |
| totalMarks | Out of 100 |

### **6. Attendance**
| Field | Description |
|-------|-------------|
| attendanceId (ObjectId) | Primary Key |
| studentId (FK) | Ref → Students |
| date | Attendance date |
| status | Present / Absent |

---
