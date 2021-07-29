# Overview
- Software Technology Project
  - Project Name: BookStore Management
  - Discription: Manage tasks in the bookstore
  - Instructor: Mr.Huynh Ngoc Tin, Mr.Tran Khanh Nguyen
- Members:
- - [Nguyen Hoai Nam](https://github.com/hoainam2310) 
  - [Đang Hoang Minh](https://github.com/danghoangminh) 
  - [Nguyen Chi Dung](https://github.com/nguyenchidungg) 
  - [Nguyen Dương Hai](https://github.com/iamthedh7) 
- Technology:
  - Language: C#
  - Enviroment: .Net Framework 4.6
  - Database: SQL Server
- Source: https://github.com/hoainam2310/BookStore_Management

# Table of contents
- [Overview](#Overview)
- [Table of contents](#Table-of-contents)
- [1. Determine the problem](#1-Determine-the-problem)
- [2. Model, Plan, Tool](#2-Plans-Model-Tools)
  - [2.1. Walterfall model](#21-Walterfall-model)
  - [2.2. Plan](#22-Plan)
  - [2.3. CASE tool](#23-case-tool)
- [3. Design data](#3-Design-data)
  - [3.1. Logic diagram](#31-Logic-diagram)
  - [3.2. Describe in detail the data types in the logic diagram](#32-Describe-in-detail-the-data-types-in-the-logic-diagram)
    - [3.2.1. TAIKHOAN table](#321-taikhoan-table)
    - [3.2.2. TACGIA table](#322-tacgia-table)
    - [3.2.3. LINHVUC table](#323-linhvuc-table)
    - [3.2.4. LOAISACH table](#324-loaisach-table)
    - [3.2.5. NHAXUATBAN table](#325-nhaxuatban-table)
    - [3.2.6. SACH table](#326-sach-table)
    - [3.2.7. KHO table](#327-kho-table)
    - [3.2.8. HOADON table](#328-hoadon-table)
    - [3.2.9. CHITIETHOADON table](#329-chitiethoadon-table)
- [4. Design interface](#4-Design-interface)
  - [4.1. Interface list](#41-Interface-list)
  - [4.2. Describe in detail of each interface](#42-Describe-in-detail-of-each-interface)
    - [4.2.1. fDangNhap interface](#421-fdangnhap-interface)
    - [4.2.2. fViewTong interface](#422-fviewtong-interface)
    - [4.2.3. fTaiKhoan interface](#423-ftaikhoan-interface)
    - [4.2.4. fThemSach interface](#424-fthemsach-interface)
    - [4.2.5. fSuaSach interface](#425-fsuasach-interface)
    - [4.2.6. fXoaSach interface](#426-fxoasach-interface)
    - [4.2.7. fThemTacGia interface](#427-fthemtacgia-interface)
    - [4.2.8. fSuaTacGia interface](#428-fsuatacgia-interface)
    - [4.2.9. fXoaTacGia interface](#429-fxoatacgia-interface)
    - [4.2.10. fLinhVuc interface](#4210-flinhvuc-interface)
    - [4.2.11. fLoaiSach interface](#4211-floaisach-interface)
    - [4.2.12. fNhaXuatBan interface](#4212-fnhaxuatban-interface)
    - [4.2.13. fKho interface](#4213-fkho-interface)
    - [4.2.14. fHoaDon interface](#4214-fhoadon-interface)
    - [4.2.15. fThongKe interface](#4215-fthongke-interface)
    - [4.2.16. fBaoCao interface](#4216-fbaocao-interface)
- [5. Architecture design](#5-Structural-design)
  - [5.1. System architecture](#51-System-architecture)
  - [5.2. Desribe in detail system architecture](#52-Desribe-in-detail-of-system-architecture)
- [6. Coding conventions](#6-Coding-conventions)
  - [6.1. Naming conventions](#61-Naming-conventions)
  - [6.2. Conventions used when coding](#62-Conventions-used-when-coding)
  - [6.3. Control prefixed](#63-Control-prefixed)
  - [6.4. Source code distribution rules](#64-Source-code-distribution-rules)
- [7. Result](#7-Result)
  - [7.1.Development environment and Deployment environment](#71-Development-environment-and-Deployment-environment)
  - [7.2. Result](#72-Result)
  - [7.3. Development](#73-Development)
# 1. Determine the problem
- Current status survey:
  - Need: Bookstores need a solution to help them manage their titles and sell books to customers.
  - Current status: A retail bookstore that uses personal memmory and notebooks to remember all titles and prices or just use Excel documents for basic management.
  - Technology used: Microsoft Excel or don't use information technology.
  - Limitations of existing software: There is no decicated application for both book sales and management.
- System requirements:
  - Add/Delete/Edit books and book information. 
  - Categorize books based on author, field, type of book and publisher.
  - Apply the payment system for bookstore.
  - Revenue statistics.
  - Manage account.
  - Manage the number of books in stock.
# 2. Model, Plan, Tool
## 2.1. Walterfall model
![](https://github.com/hoainam2310/BookStore_Management/blob/main/model.png)

This model consists of successive processing stages as follows:

- Analysis: Determine the functional and non-functional requirements required by the software system.

- Requirement specification: Determine the software system that meets the requirements of the customer. This phase performs analysis and design of the software system.
- Design: Build model of software, design data and interface.

- Development: Impelemt product based on requirement specification and module design document.

- Testing and Integration: Perform group testing of components and system testing. Check for possible exceptions and fix them.
## 2.2. Plan
![](https://github.com/hoainam2310/BookStore_Management/blob/main/roadmap.png)

The plan consists of 5 stages:
- Analysis (03/04 - 11/04)

- Requirement (11/04 v 24/04)

- Design (24/04 - 21/05)

- Development (21/05 - 05/07)

- Testing (05/07 - 10/07)

## 2.3. CASE tool
- IDE: Visual Studio

- Code Repositories: Github

- Issues tracking: Github
# 3. Design Data
## 3.1. Logic diagram
![](https://github.com/hoainam2310/BookStore_Management/blob/main/database.png)
## 3.2.Describe in detail the data types in the logic diagram
### 3.2.1. TAIKHOAN table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | USERNAME       | nvarchar(20)  | Selt-generated              | System login name           |
| 2       | PASS_WORD      | nvarchar(100) | Not null                    | System login password       |
### 3.2.2. TACGIA table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | MATG           | char(7)       | Selt-generated              | Author identification code  |
| 2       | TENTG          | nvarchar(40)  | Not null                    | Author name                 |
| 3       | NAMSINH        | date          | No constraint               | Year of birth               |
| 4       | NAMMAT         | date          | No constraint               | Year of death               |
| 5       | QUEQUAN        | nvarchar(20)  | No constraint               | Hometown                    |
### 3.2.3. LINHVUC table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | TENLINHVUC     | nvarchar(30)  | Not Null                    | Tên lĩnh vực sách           |
### 3.2.4. LOAISACH table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | TENLOAISACH    | nvarchar(30)  | Not Null                    | Tên loại sách               |
### 3.2.5. NHAXUATBAN table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | TENNHAXUATBAN  | nvarchar(50)  | Not Null                    | Tên nhà xuất bản sách       |
### 3.2.6. SACH table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | MASACH         | char(7)       | Selt-generated              | Mã phân biệt sách           |
| 2       | TENSACH        | nvarchar(100) | Not null                    | Tên của sách                |
| 3       | MATG           | char(7)       | Not Null, Existed           | Mã phân biệt tác giả        |
| 4       | TENLINHVUC     | nvarchar(30)  | Not Null, Existed           | Tên lĩnh vực sách           |
| 5       | TENLOAISACH    | nvarchar(30)  | Not Null, Existed           | Tên loại sách               |
| 6       | GIAMUA         | int           | >= 0                        | Giá nhập sách               |
| 7       | GIABIA         | int           | >= 0                        | Giá bán sách                |
| 8       | LANTAIBAN      | int           | >= 0                        | Số lần tái bản của sách     |
| 9       | TENNHAXUATBAN  | nvarchar(50)  | Not Null, Existed           | Tên nhà xuất bản sách       |
| 10      | NAMXUATBAN     | datetime      | Not Null, Existed           | Năm sách được xuất bản      |
### 3.2.7. KHO table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | MASACH         | char(7)       | Existed                     | Mã phân biệt sách           |
| 2       | SOLUONG        | int           | >= 1                        | Số lượng sách còn           |
### 3.2.8. HOADON table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | MAHOADON       | char(7)       | Selt-generated              | Mã phân biệt hóa đơn        |
| 2       | TENKHACHHANG   | nvarchar(50)  | Not null                    | Tên của khách hàng          |
| 3       | NGAYLAP        | datetime      | Selt-generated              | Ngày lập hóa đơn            |
| 4       | TONGTIEN       | decimal(10, 2)| >= 0                        | Tổng tiền hóa đơn           |
### 3.2.9. CHITIETHOADON table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | MAHOADON       | char(7)       | Existed                     | Mã phân biệt hóa đơn        |
| 2       | MASACH         | char(7)       | Existed                     | Mã phân biệt sách           |
| 3       | SOLUONG        | int           | >= 1                        | Số lượng sách mua           |
| 4       | GIATIEN        | int           | >= 0                        | Giá bán sách                |
| 5       | THANHTIEN      | int           | >= 0                        | Giá bán sách x Số lượng sách|
# 4. Thiết kế giao diện
## 4.1. Danh sách màn hình
| Numbers | Interface Name | Meaning/Notes                                                                          |
|---------|----------------|------------------------------------------------------------------------------------------|
| 1       | fDangNhap      | Đăng nhập vào hệ thống bằng username và password                                         |
| 2       | fViewTong      | Màn hình chính, hiển thị danh sách các đầu sách hiện có                                  |
| 3       | fTaiKhoan      | Hiển thị danh sách user của hệ thống và chỉnh sửa mật khẩu                               |
| 4       | fThemSach      | Nhập thông tin để thêm sách                                                              |
| 5       | fSuaSach       | Sửa thông tin của sách theo mã sách                                                      |
| 6       | fXoaSach       | Xóa thông tin của sách theo mã sách                                                      |
| 7       | fThemTacGia    | Nhập thông tin để thêm tác giả                                                           |
| 8       | fSuaTacGia     | Sửa thông tin của tác giả theo mã tác giả                                                |
| 9       | fXoaTacGia     | Xóa thông tin của tác giả theo mã tác giả                                                |
| 10      | fLinhVuc       | Thêm và xóa lĩnh vực sách                                                                |
| 11      | fLoaiSach      | Thêm và xóa loại sách                                                                    |
| 12      | fNhaXuatBan    | Thêm và xóa nhà xuất bản sách                                                            |
| 13      | fKho           | Hiển thị số lượng sách còn trong kho và thêm số lượng sách                               |
| 14      | fHoaDon        | Hiển thị hóa đơn và chi tiết hóa đơn. Thêm/xóa/sửa hóa đơn và chi tiết hóa đơn           |
| 15      | fThongKe       | Hiển thị danh sách hóa đơn trong khoảng ngày chọn                                        |
| 16      | fBaoCao        | Hiển thị danh sách các đầu sách đã bán được, doanh thu, lợi nhuận trong khoảng ngày chọn |
## 4.2. Mô tả chi tiết mỗi màn hình
### 4.2.1. Màn hình fDangNhap
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/DangNhap.png)

Người dùng điền thông tin Username/Password để đăng nhập. Nếu đăng nhập thất bại quá 3 lần sẽ tự tắt chương trình.
### 4.2.2. Màn hình fViewTong
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/Quanlynhasach.png)

Hiển thị những đầu sách có trong database, doanh thu và số lượng khách trong ngày hôm đó. Menu ở trên chứa các chức năng của chương trình.
### 4.2.3. Màn hình fTaiKhoan
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/ThayDoiThongTinAcc.png)

Cho phép thay đổi mật khẩu của tài khoản, yêu cầu nhập đúng mật khẩu cũ khi muốn thay đổi mật khẩu mới.
### 4.2.4. Màn hình fThemSach
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/ThemSach.png)

Cho phép thêm đầu sách mới vào database. Yêu cầu nhập đầy đủ thông tin, nếu không sẽ báo lỗi nhập thiếu và yêu cầu bổ sung.
### 4.2.5. Màn hình fSuaSach
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/SuaSach.png)

Cho phép sửa thông tin sách trong database. Yêu cầu nhập đầy đủ thông tin, nếu không sẽ báo lỗi nhập thiếu và yêu cầu bổ sung.
### 4.2.6. Màn hình fXoaSach
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/XoaSach.png)

Cho phép xóa sách trong database. Chọn sách cần xóa trong list sách hiển thị.
### 4.2.7. Màn hình fThemTacGia
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/ThemTG.png)

Cho phép thêm tác giả mới vào database. Yêu cầu nhập tên tác giả, nếu không sẽ báo lỗi nhập thiếu và yêu cầu bổ sung. Đối với ô Quê Quán, Năm Sinh, Năm Mất nếu không có thì phải chọn nút 'CHƯA RÕ' không sẽ báo lỗi thiếu thông tin.
### 4.2.8. Màn hình fSuaTacGia
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/SuaTG.png)

Cho phép sửa thông tin tác giả trong database. Yêu cầu nhập tên tác giả, nếu không sẽ báo lỗi nhập thiếu và yêu cầu bổ sung. Đối với ô Quê Quán, Năm Sinh, Năm Mất nếu không có thì phải chọn nút 'CHƯA RÕ' không sẽ báo lỗi thiếu thông tin.
### 4.2.9. Màn hình fXoaTacGia
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/XoaTG.png)

Cho phép xóa tác giả trong database. Chọn tác giả cần xóa trong list sách hiển thị.
### 4.2.10. Màn hình fLinhVuc
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/LinhVuc.png)

Cho phép thêm lĩnh vực mới vào database. Nếu muốn xóa thì chọn lĩnh vực cần xóa ở menu bên dưới và bấm nút xóa.
### 4.2.11. Màn hình fLoaiSach
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/LoaiSach.png)

Cho phép thêm loại sách mới vào database. Nếu muốn xóa thì chọn loại sách cần xóa ở menu bên dưới và bấm nút xóa.
### 4.2.12. Màn hình fNhaXuatBan
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/NXB.png)

Cho phép thêm nhà xuất bản mới vào database. Nếu muốn xóa thì chọn nhà xuất bản cần xóa ở menu bên dưới và bấm nút xóa.
### 4.2.13. Màn hình fKho
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/Kho.png)
Gồm 2 phần:
- Phần trên: cho phép sửa số lượng sách có trong kho hoặc xóa luôn sách.
- Phần dưới: thêm số lượng cho đầu sách có trong kho.
### 4.2.14. Màn hình fHoaDon
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/HoaDon.png)
Gồm 2 phần:
- Phần trên: hiển thị danh sách hóa đơn hiện có trong database cho phép xóa/sửa hóa đơn và xem chi tiết hóa đơn đó ở bảng kế bên.
- Phần dưới: thêm/sửa hóa đơn, thêm vật phẩm vô hóa đơn, yêu cầu nhập đầy đủ thông tin.
### 4.2.15. Màn hình fThongKe
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/ThongKe.png)
Chọn khoảng ngày cần thống kê bán hàng, phần mềm sẽ hiển thị những hóa đơn trong khoảng ngày được chọn.
### 4.2.16. Màn hình fBaoCao
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/Scene/BaoCao.png)
Xuất báo cáo chi tiết về số lượng bán đượccác loại sách, doanh thu và lợi nhuận trong khoảng ngày đã chọn ở màn hình fThongKe.
# 5. Thiết kế kiến trúc
## 5.1. Kiến trúc hệ thống
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/layer.png)
| Thành phần | Diễn giải                         |
|------------|-----------------------------------|
| Client     | Ứng dụng tương tác với người dùng |
| Data       | Nơi chứa dữ liệu của hệ thống     |
## 5.2. Mô tả chi tiết kiến trúc hệ thống
![](https://github.com/danghoangminh/BookStoreManagement/blob/finalcode/folderview.png)
- Ứng dụng được thiết kế theo mô hình 2 lớp (được viết chung trong 1 project) gồm:
  - View xử lý giao diện và xử lý tác vụ.
  - DAO gọi các truy xuất từ csdl (SQL).
# 6. Quy ước viết mã
## 6.1. Quy tắc đặt tên
| Kiểu        | Mô tả           | Ví dụ        |
|-------------|-----------------|--------------|
| Pascal Case | Chữ cái đầu tiên trong từ định danh và chữ cái đầu tiên của mỗi từ nối theo sau phải được viết hoa. Sử dụng Pascal Case để đặt tên cho một tên có từ 3 ký tự trở lên | `CodingConv` |
| Camel Case  | Chữ cái đầu tiên trong từ định danh là chữ thường và chữ cái đầu tiên của mối từ nối theo sau phải được viết hoa          | `codingConv` |
| Uppercase   | Tất cả các ký tự trong từ định danh phải được viết hoa. Sử dụng quy tắc này đối với tên định danh có từ 2 ký tự trở xuống | `System.IO ` |
## 6.2. Quy tắc sử dụng khi code
| Loại            | Kiểu        | Ví dụ                 | Ghi chú                  |
|-----------------|-------------|-----------------------|--------------------------|
| Tên biến        | Camel Case  | `firstName`           | Danh từ                  |
| Hằng số         | Uppercase   | `FIRST_WEEK_DAY`      | Có gạch chân giữa các từ |
| Tên class, enum | Pascal Case | `CreateUser`          | Danh từ                  |
| Tham số         | Camel Case  | `displayTime`         | Danh từ                  |
| Thuộc tính      | Pascal Case | `BackgroundColor`     | Danh từ                  |
| Phương thức     | Pascal Case | `GetAge()`            | Có gạch chân giữa các từ |
| Sự kiện         | Pascal Case | `SelectedIndexChanged`| Có gạch chân giữa các từ |
| Giao diện       | Pascal Case | `IButtonControl`      | Có gạch chân giữa các từ |
- Tránh thêm các tiền tố hoặc hậu tố dư thừa vô nghĩa:
  - Không nên:
  ```
  enum BorderEnum { ... }
  class CHuman { ... }
  ```
  - Nên:
  ```
  enum Border { ... }
  class Human { ... }
  ```
- Không thêm tên lớp chứa vào tên thuộc tính:
  - Không nên:
  ```
  Animal.WeightAnimal
  ```
  - Nên:
  ```
  Animal.Weight
  ```
- Tên biến, phương thức bool phải thể hiện được ý nghĩa nếu trả về true hoặc false. Nên sử dụng tiền tố “Is” “Can” “Has” trước tên biến, phương thức:
  - Không nên:
  ```
  bool CheckAdmin(int n) { }
  bool Expired() { }
  bool checked = true;
  ```
  - Nên:
  ```
  bool IsAdmin(int n) { }
  bool IsExpired() { }
  bool isChecked = true;
  ```
- Không dùng các tên giống nhau(chỉ phân biệt kiểu chữ in hoa hay thường). Ta khó nhận ra các định danh nhất là khi trong cùng ngữ cảnh và chỉ phân biệt các định danh bằng kiểu chữ in hoa/thường.
- Không tạo 2 namespace cùng tên và chỉ khác nhau ở kiểu chữ viết(chữ hoa/Chữ thường), ví dụ:
  ```
  Namespace SunAsterisk
  Namespace sunAsterisk
  ```
- Không nên xây dựng 1 phương thức với các tham số có cùng tên và chỉ khác nhau kiểu chữ, ví dụ:
  ```
  void MyFunction(string a, string A)
  ```
- Không xây dựng 1 kiểu với các tên property giống nhau và chỉ phân biệt ở kiểu chữ, ví dụ:
  ```
  int Color {get, set}
  int COLOR {get, set}
  ```
## 6.3. Tiền tố một số control
Bắt buộc đặt tên cho tất cả các control có tham gia xử lý dưới nền. Một số control được đặt theo kiểu Pascal với phần tiền tố như sau:
| Control      | Tiền tố | Ví dụ       |
|--------------|---------|-------------|
| Panel        | pnl     | pnlGroup    |
| Checkbox     | chk     | chkReadOnly |
| ComboBox     | cbo     | cboEnglish  |
| Button       | btn     | btnSave     |
| Dialog       | dlg     | dlgFileOpen |
| Form         | frm     | frmLogin    |
| Textbox      | txb     | txbUser     |
| User Control | uc      | ucBooks     |
| Label        | lbl     | lblName     |
| DataGridView | dgv     | dgvBook     |
## 6.4. Quy định phân bố mã nguồn
- Mỗi file mã nguồn chỉ chứa duy nhất một class. Tên class chính phải trùng với tên file mã nguồn. Ví dụ: Class Student sẽ được chứa trong file Student.cs.
- Với các kiểu enum, struct độc lập đơn giản ngoài class có thể được khai báo trong một file mã nguồn riêng hoặc trong file mã nguồn của class khác.
- Interface phải được khai báo trong một file mã nguồn riêng.
- Thứ tự khai báo:
  - Khối khai báo thư viện
  ```
  using System.Data;
  using System.Drawing;
  ```
  - Khai báo namespace
  ```
  namespace SQLBackup;
  ```
  - Khai báo các struct/enum độc lập (nếu có)
  ```
  public enum HumanClass { A, B, C, D, E }
  ```
  - Khai báo lớp chính
  ```
  public class Student : Human {}
  ```
# 7. Kết quả thực hiện
## 7.1. Môi trường phát triển và Môi trường triển khai
- Môi trường phát triển ứng dụng:
  - Hệ điều hành: Microsoft Windows 10
  - Hệ quản trị cơ sở dữ liệu: Microsoft SQL Server
  - Công cụ phân tích thiết kế: Visual Studio 2019
  - Công cụ xây dựng ứng dụng: Visual Studio 2019
- Môi trường triển khai ứng dụng:
  - Hệ điều hành: Microsoft Windows
  - Cần cài đặt .Net Framework 4.0 hoặc cao hơn
  - Để chương trình hoạt động cần có đủ các dll trong folder dll
## 7.2. Kết quả đạt được
- Chương trình đã được hoàn thiện hầu hết các chức năng, nhưng vẫn có những chức năng chưa được hoàn thiện như: Thêm tài khoản, Xuất file báo cáo dạng PDF hoặc Excel.
## 7.3. Hướng phát triển
- Hoàn thiện các chức năng và giao diện chưa hoàn tất.
- Cải thiện hiệu năng của chương trình để phù hợp với thực tiễn.
- Bổ sung các chức năng liên quan đến CSDL: backup/restore.
- Bổ sung phân quyền tài khoản cho các chức năng của phần mềm.
