# API Endpoints - TesloShop Backend

## Authentication

### 1. Register User
**Endpoint:** `POST /api/auth/register`

**Headers:**
```
Authorization: Bearer ${token}
```

**Body:**
```json
{
  "email": "test3@google.com",
  "password": "Abc123",
  "fullName": "Sebastian"
}
```

---

### 2. Login
**Endpoint:** `POST /api/auth/login`

**Body:**
```json
{
  "email": "test4@google.com",
  "password": "Abc123"
}
```

---

### 3. Check Authentication Status
**Endpoint:** `GET /api/auth/check-status`

**Headers:**
```
Authorization: Bearer ${token}
```

---

## Data Management

### 4. Seed Database
**Endpoint:** `GET /api/seed`

**Description:** Crea los primeros usuarios de ejemplo en la base de datos.

---

**Base URL:** `http://localhost:3000`