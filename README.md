📧 EmailListMVC


**📖 Giới thiệu**

  EmailListMVC là một ứng dụng web đơn giản được xây dựng theo mô hình MVC (Model - View - Controller).
Ứng dụng cho phép người dùng nhập thông tin cá nhân (Email, First Name, Last Name) để đăng ký vào danh sách email.

**Quy trình hoạt động:**

  1. Người dùng truy cập trang index.html để nhập thông tin.

  2. Khi nhấn nút Join Now, dữ liệu được gửi đến Servlet để xử lý.

  3. Người dùng được chuyển hướng đến trang thanks.jsp hiển thị lại thông tin đã nhập.

  4. Nếu muốn thêm email khác, người dùng có thể nhấn Return để quay lại trang đăng ký.

**📂 Cấu trúc thư mục**
EmailListMVC/
│── Deployment Descriptor: EmailListMVC
│── JAX-WS Web Services
│── Java Resources
│── build/
│
└── src/
    └── main/
        ├── java/
        │   └── murach/
        │       ├── business/
        │       │   └── User.java           # Model: lớp mô tả User (email, firstname, lastname)
        │       ├── data/
        │       │   └── UserDB.java         # Model: xử lý lưu trữ User (giả lập DB)
        │       └── email/
        │           └── EmailListServlet.java # Controller: xử lý request/response
        │
        └── webapp/
            ├── META-INF/
            │   └── MANIFEST.MF
            ├── WEB-INF/
            │   ├── lib/                    # Chứa thư viện hỗ trợ (nếu có)
            │   └── web.xml                 # Cấu hình servlet & routing
            ├── index.html                  # View: form nhập email
            ├── main.css                    # View: stylesheet cho giao diện
            └── thanks.jsp                  # View: trang cảm ơn hiển thị thông tin đã nhập

**🖥️ Chức năng chi tiết**
1. Trang Index (index.html)

URL: http://localhost:8080/EmailListMVC/index.html

Chức năng: hiển thị form nhập liệu.

_Các trường nhập:_

  Email

  First Name

  Last Name

_Nút bấm:_

  Join Now → gửi dữ liệu đến EmailListServlet để xử lý.

2. Controller EmailListServlet.java

  Nhận dữ liệu từ index.html.

  Tạo đối tượng User từ dữ liệu nhập.

  Gửi dữ liệu sang thanks.jsp.

3. Trang Thanks (thanks.jsp)

  Hiển thị lại thông tin mà người dùng vừa nhập.

  Có nút Return quay lại index.html để nhập thêm email mới.

**📸 Giao diện minh họa**
Trang 1: Form đăng ký email

<img width="630" height="323" alt="image" src="https://github.com/user-attachments/assets/558a4553-bf18-40db-9d3c-685dc6bec89c" />

Trang 2: Trang cảm ơn (hiển thị thông tin đã nhập)

<img width="938" height="402" alt="image" src="https://github.com/user-attachments/assets/fce0e4a5-bbea-4164-bb5d-61b66f22a9f3" />

**⚙️ Công nghệ sử dụng**

  Java Servlet (Controller)

  JSP (View)

  HTML/CSS (Giao diện)

  Mô hình MVC để tách biệt logic và giao diện

**🚀 Cách chạy project**

  Import project vào Eclipse hoặc IDE hỗ trợ Java EE.

  Cấu hình server Tomcat (ví dụ Tomcat 9.0).

  Deploy project EmailListMVC lên server.

  Truy cập ứng dụng tại: http://localhost:8080/EmailListMVC/index.html
