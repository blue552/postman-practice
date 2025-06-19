# 🚀 Postman Practice

## 📌 Giới thiệu

**Postman** là một công cụ mạnh mẽ giúp lập trình viên và tester dễ dàng gửi các yêu cầu HTTP (GET, POST, PUT, DELETE...) đến API, kiểm tra phản hồi (response) và tự động hóa kiểm thử. Postman hỗ trợ:

- Giao diện đồ họa thân thiện
- Tạo collection chứa nhiều API
- Sử dụng biến môi trường (`{{base_url}}`, `{{token}}`)
- Viết test kiểm tra phản hồi tự động (test scripts)
- Chia sẻ & lưu trữ qua Postman cloud

---

## 📝 Mô tả bài thực hành

Bài thực hành sử dụng công cụ Postman để kiểm thử các phương thức HTTP cơ bản thông qua API mẫu từ `https://reqres.in`.

---

## ✅ Nội dung đã thực hiện

- Gửi request `GET`, `POST`, `PUT`, `DELETE` tới API mẫu
- Tạo **Collection** trong Postman
- Viết test case đơn giản với `pm.test()`
- Sử dụng **Environment Variables** trong Postman
- Kiểm thử API có xác thực `Bearer Token`

---

## 📸 Hình ảnh minh họa

### 1️⃣ Tạo một request cơ bản (GET)

Gửi `GET` tới danh sách người dùng:

```http
GET https://reqres.in/api/users?page=2
```

<div align="center">
<img src="./image-5.png" alt="GET request" width="800"/>
</div>

---

### 2️⃣ Test case `POST` – Đăng nhập nhưng thiếu password

- **Base URL:** `https://reqres.in/api/login`  
- **Body gửi đi:**
```json
{
  "email": "peter@klaven"
}
```
- **Kết quả mong đợi:**
```json
{
  "error": "Missing password"
}
```

<div align="center">
<img src="./image-7.png" alt="POST test case" width="800"/>
</div>

---

### 3️⃣ Test case `PUT` – Cập nhật người dùng

- Gửi `PUT` đến: `https://reqres.in/api/users/2`
- **Body ví dụ:**
```json
{
  "name": "Baonguyen",
  "job": "Tester"
}
```
- **Yêu cầu API key nếu cần.**

<div align="center">
<img src="./image-6.png" alt="PUT request" width="800"/>
</div>

---

### 4️⃣ Test case `DELETE` – Xoá người dùng

- **Base URL:** `https://reqres.in/api/users/2`
- **Phản hồi mong đợi:** `204 No Content`

<div align="center">
<img src="./image-8.png" alt="DELETE request" width="800"/>
</div>

---

## 🎯 Kết quả & học được gì?

- Hiểu rõ cách hoạt động của các HTTP methods: `GET`, `POST`, `PUT`, `DELETE`
- Biết cách kiểm thử nhanh các API với Postman
- Viết được test case đơn giản để kiểm tra response
- Làm quen với biến môi trường trong Postman (`{{token}}`, `{{base_url}}`)
- Sử dụng API công khai (public API) như `reqres.in` để luyện tập mà không cần backend riêng

---

## 📚 Tài liệu tham khảo

- [Postman Official Website](https://www.postman.com/)
- [Postman Learning Center](https://learning.postman.com/)
- [ReqRes - Test API](https://reqres.in/)