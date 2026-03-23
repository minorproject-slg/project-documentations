# 🔐 **1. Auth Service (`/auth`)**

```http
POST   /auth/register
POST   /auth/login
POST   /auth/logout
GET    /auth/me              # current user info
GET    /auth/validate        # token validation
```

---

# 👥 **2. User Service**

## 👤 Students (`/students`)

```http
GET    /students
GET    /students/{id}
POST   /students
PUT    /students/{id}
DELETE /students/{id}

PATCH  /students/{id}/status        # active/inactive
POST   /students/{id}/documents     # upload docs
GET    /students/{id}/documents
```

---

## 👨‍🏫 Faculty (`/faculty`)

```http
GET    /faculty
GET    /faculty/{id}
POST   /faculty
PUT    /faculty/{id}
DELETE /faculty/{id}

POST   /faculty/{id}/assign-subject
GET    /faculty/{id}/subjects
```

---

# 🎓 **3. Academic Service**

## 🏫 Departments

```http
GET    /departments
POST   /departments
```

---

## 📚 Courses

```http
GET    /courses
GET    /courses/{id}
POST   /courses
PUT    /courses/{id}
```

---

## 📖 Subjects

```http
GET    /subjects
POST   /subjects
PUT    /subjects/{id}

POST   /subjects/{id}/assign-department
```

---

## 📝 Attendance

```http
POST   /attendance                 # mark attendance
GET    /attendance/student/{id}
GET    /attendance/class/{id}

GET    /attendance/student/{id}/percentage
GET    /attendance/low            # low attendance list
```

---

## 🧪 Exams

```http
GET    /exams
POST   /exams
```

---

## 📊 Marks & Results

```http
POST   /marks
GET    /marks/{studentId}

GET    /results/{studentId}
GET    /results/{studentId}/gpa
```

---

# 💰 **4. Finance Service (`/fees`)**

```http
GET    /fees/structure
POST   /fees/structure

GET    /fees/{studentId}
POST   /fees/pay

GET    /fees/transactions
GET    /fees/receipt/{transactionId}
```

---

# 🔔 **5. Notification Service (`/notifications`)**

```http
GET    /notifications
POST   /notifications

POST   /notifications/email
```

---

# 📊 **6. Dashboard Service (or API aggregation)**

```http
GET    /dashboard/summary
GET    /dashboard/activity
```

👉 Returns:

* total students
* total faculty
* attendance overview
* recent logs

---

# 🧾 **7. Audit & Logs (`/logs`)**

```http
GET    /logs
POST   /logs
```

---

# 🌐 **Final API Gateway Structure**

```http
/api/auth/...
/api/students/...
/api/faculty/...
/api/courses/...
/api/attendance/...
/api/results/...
/api/fees/...
/api/notifications/...
/api/dashboard/...
/api/logs/...
```
