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

## Obtener Productos
**Endpoint:** `GET /api/products`

**Descripción:** Obtiene una lista de productos con paginación.

**Query Parameters:**
- `limit` (optional): Número de productos a retornar (default: 20)
- `offset` (optional): Número de productos a omitir (default: 0)

**Ejemplo de URL:**
localhost:3000/api/products?limit=20&offset=20

Esta url retornará los productos del 21 al 40.

---

## Obtener Producto por ID
**Endpoint:** `GET /api/products/:id`

**Descripción:** Cada producto tiene su ID único y con esa url puedes obtener un producto específico por su ID.

**Ejemplo de URL:**
localhost:3000/api/products/b68113a4-bb6d-48f7-b45e-04210cca57a3

Esta url retornará el producto con el ID `b68113a4-bb6d-48f7-b45e-04210cca57a3`.

---

## Cargar Imagen de Producto
**Endpoint:** `POST /api/files/product`

**Descripción:** Permite subir una imagen para un producto específico. La imagen se asocia al producto mediante su ID.

**Body:** Form-Data (solo form en Thunder Client)  con el campo `file` y la dirección de la imagen a subir.
sí todo está correcto, la imagen se subirá y retornará un id-img.png.

---

## Obtener Imagen de Producto
**Endpoint:** `GET /api/files/product/:id`

**Descripción:** Permite obtener la imagen de un producto específico mediante su ID.

---

## User Management

### 4. Seed Database
**Endpoint:** `GET /api/seed`

**Description:** Crea los primeros usuarios de ejemplo en la base de datos.

---

**Base URL:** `http://localhost:3000`