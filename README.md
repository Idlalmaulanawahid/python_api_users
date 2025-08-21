# User API

API sederhana untuk manajemen data User menggunakan **FastAPI**.

## Fitur

- **Create User**  
  Tambah user baru.

- **Read Users**  
  Lihat semua user.

- **Read User by ID**  
  Lihat detail user berdasarkan ID.

- **Update User**  
  Update data user berdasarkan ID.

- **Delete User**  
  Hapus user berdasarkan ID.

## Instalasi

1. **Clone repository**  
   ```
   git clone <repo-url>
   cd user-api
   ```

2. **Buat virtual environment**  
   ```
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies**  
   ```
   pip install fastapi uvicorn
   ```

## Menjalankan Server

```
uvicorn main:app --reload
```

Akses dokumentasi otomatis di:  
[http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

## Contoh Request

### Create User

```json
POST /users/
{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com"
}
```

### Get All Users

```
GET /users/
```

### Get User by ID

```
GET /users/1
```

### Update User

```json
PUT /users/1
{
  "id": 1,
  "name": "Jane Doe",
  "email": "jane@example.com"
}
```

### Delete User

```
DELETE /users/1
```

---

**Catatan:**  
Data user hanya disimpan di memori (tidak permanen).