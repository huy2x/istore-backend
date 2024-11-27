# iStore Backend API

## Giới thiệu
iStore Backend API là phần server của dự án web thương mại điện tử chuyên về sản phẩm Apple. Được xây dựng bằng Java Spring Boot, cung cấp RESTful API cho frontend.

## Công nghệ sử dụng
- Java 17
- Spring Boot 3.x
- Spring Security
- Spring Data JPA
- MySQL
- JWT
- Swagger
- Maven

## Cấu trúc thư mục
```
src/
├── main/
│   ├── java/
│   │   └── com/
│   │       └── istore/
│   │           ├── IStoreApplication.java
│   │           ├── config/
│   │           │   ├── SecurityConfig.java
│   │           │   ├── SwaggerConfig.java
│   │           │   └── WebConfig.java
│   │           ├── controller/
│   │           │   ├── AuthController.java
│   │           │   ├── ProductController.java
│   │           │   └── OrderController.java
│   │           ├── dto/
│   │           │   ├── request/
│   │           │   └── response/
│   │           ├── entity/
│   │           │   ├── User.java
│   │           │   ├── Product.java
│   │           │   └── Order.java
│   │           ├── repository/
│   │           ├── service/
│   │           │   ├── impl/
│   │           │   └── interfaces/
│   │           ├── security/
│   │           └── util/
│   └── resources/
│       ├── application.properties
│       ├── application-dev.properties
│       └── application-prod.properties
└── test/
    └── java/
        └── com/
            └── istore/
```

## Cài đặt và Chạy

### Yêu cầu hệ thống
- JDK 17 trở lên
- Maven
- MySQL

### Các bước cài đặt

1. Clone repository
```bash
git clone https://github.com/huy2x/istore-backend.git
cd istore-backend
```

2. Cấu hình database
- Tạo database MySQL
- Cập nhật thông tin database trong `application.properties`

3. Build project
```bash
mvn clean install
```

4. Chạy ứng dụng
```bash
mvn spring-boot:run
```

Ứng dụng sẽ chạy tại `http://localhost:8080`

### API Documentation
Swagger UI: `http://localhost:8080/swagger-ui.html`

## Tính năng chính
- [x] Xác thực và phân quyền với JWT
- [x] CRUD sản phẩm
- [x] Quản lý đơn hàng
- [x] Quản lý người dùng
- [ ] Tích hợp thanh toán
- [ ] Quản lý file
- [ ] Email service

## Contributing
1. Fork project
2. Tạo branch mới (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Tạo Pull Request

## License
[Apache-2.0 License](LICENSE)
