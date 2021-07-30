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
- [2. Model, Plan, Tool](#2-Model-Plan-Tool)
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
- [5. Design architecture](#5-Design-architecture)
  - [5.1. System architecture](#51-System-architecture)
  - [5.2. Desribe in detail system architecture](#52-Desribe-in-detail-system-architecture)
- [6. Coding conventions](#6-Coding-conventions)
  - [6.1. Naming conventions](#61-Naming-conventions)
  - [6.2. Conventions used when coding](#62-Conventions-used-when-coding)
  - [6.3. Control prefixed](#63-Control-prefixed)
  - [6.4. Source code distribution rules](#64-Source-code-distribution-rules)
- [7. Result](#7-Result)
  - [7.1. Development environment and Deployment environment](#71-Development-environment-and-Deployment-environment)
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
## 3.2. Describe in detail the data types in the logic diagram
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
| 1       | TENLINHVUC     | nvarchar(30)  | Not Null                    | Name of book field          |
### 3.2.4. LOAISACH table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | TENLOAISACH    | nvarchar(30)  | Not Null                    | Name of book category       |
### 3.2.5. NHAXUATBAN table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | TENNHAXUATBAN  | nvarchar(50)  | Not Null                    | Name of book producer       |
### 3.2.6. SACH table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | MASACH         | char(7)       | Selt-generated              | Book identification code    |
| 2       | TENSACH        | nvarchar(100) | Not null                    | Name of book                |
| 3       | MATG           | char(7)       | Not Null, Existed           | Author identification code  |
| 4       | TENLINHVUC     | nvarchar(30)  | Not Null, Existed           | Name of book field          |
| 5       | TENLOAISACH    | nvarchar(30)  | Not Null, Existed           | Name of book category       |
| 6       | GIAMUA         | int           | >= 0                        | Book entry price            |
| 7       | GIABIA         | int           | >= 0                        | Book sell price             |
| 8       | LANTAIBAN      | int           | >= 0                        | Number of reprints          |
| 9       | TENNHAXUATBAN  | nvarchar(50)  | Not Null, Existed           | Name of book producer       |
| 10      | NAMXUATBAN     | datetime      | Not Null, Existed           | The year the book was published      |
### 3.2.7. KHO table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | MASACH         | char(7)       | Existed                     | Book identification code    |
| 2       | SOLUONG        | int           | >= 1                        | Number of books remaining   |
### 3.2.8. HOADON table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | MAHOADON       | char(7)       | Selt-generated              | Bill identification code    |
| 2       | TENKHACHHANG   | nvarchar(50)  | Not null                    | Name of customer            |
| 3       | NGAYLAP        | datetime      | Selt-generated              | Bill date                   |
| 4       | TONGTIEN       | decimal(10, 2)| >= 0                        | Total amount in bill        |
### 3.2.9. CHITIETHOADON table
| Numbers | Attribute Name | Type          | Constraint                  | Meaning/Notes               |
|---------|----------------|---------------|-----------------------------|-----------------------------|
| 1       | MAHOADON       | char(7)       | Existed                     | Bill identification code    |
| 2       | MASACH         | char(7)       | Existed                     | Book identification code    |
| 3       | SOLUONG        | int           | >= 1                        | Number of books purcheased  |
| 4       | GIATIEN        | int           | >= 0                        | Book sell price             |
| 5       | THANHTIEN      | int           | >= 0                        | Book sell price x Number of books|
# 4. Design interface
## 4.1. Interface list
| Numbers | Interface Name | Meaning/Notes                                                                          |
|---------|----------------|------------------------------------------------------------------------------------------|
| 1       | fDangNhap      | Log in to the system with username and password                                          |
| 2       | fViewTong      | The main screen shows a list of available titles                                         |
| 3       | fTaiKhoan      | Display the list of system users and edit passwords                                      |
| 4       | fThemSach      | Enter information to add books                                                           |
| 5       | fSuaSach       | Edit the information of the book by the book code                                        |
| 6       | fXoaSach       | Delete the information of the book by the book code                                      |
| 7       | fThemTacGia    | Enter information to add authors                                                         |
| 8       | fSuaTacGia     | Edit the information of the author by the author code                                    |
| 9       | fXoaTacGia     | Delete the information of the author by the author code                                  |
| 10      | fLinhVuc       | Add and remove book field names                                                          |
| 11      | fLoaiSach      | Add and remove book category names                                                       |
| 12      | fNhaXuatBan    | Add and remove publisher names                                                            |
| 13      | fKho           | Show the number of books in stock and add the number of books                            |
| 14      | fHoaDon        | Show bill and bill details. Add/Remove/Edit bills and bill details                       |
| 15      | fThongKe       | Show a list of bills for a selected date range                                           |
| 16      | fBaoCao        | Show a list of sold titles, sales, and profits in the selected date range                |
## 4.2. Describe in detail of each interface
### 4.2.1. fDangNhap interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/DangNhap.png)

User fills in Username/Password information to log in. If the login fails more than 3 times, the program will automatically shut down.
### 4.2.2. fViewTong interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/Quanlynhasach.png)

Displays the titles in the database, the revenue and the number of customers that day. The Menu above contains the program's functions. 
### 4.2.3. fTaiKhoan interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/ThayDoiThongTinAcc.png)

Allows to change the account's password, requires entering the correct old password when you want to change the new password.
### 4.2.4. fThemSach interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/ThemSach.png)

Allows adding new titles to the database. Please enter complete information, otherwise, you'll receive a missing input error and ask additional information.
### 4.2.5. fSuaSach interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/SuaSach.png)

Allows editting book information in the database. Please enter complete information, otherwise, you'll receive a missing input error and ask for additional information.
### 4.2.6. fXoaSach interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/XoaSach.png)

Allows deleting books in the database. Select the book to delete in the list of displayed books.
### 4.2.7. fThemTacGia interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/ThemTG.png)

Allows adding new authors to the database. Please enter the author's name, otherwise it will report a missing input error and add for additional information. For the box "Hometown", "Year of birth", "Year of death", if it's not available, you must select the "unknown" button or it will report an error of missing information.
### 4.2.8. fSuaTacGia interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/SuaTG.png)

Allows editting author information in the database. Please enter the author's name, otherwise it will report a missing input error and add for additional information. For the box "Hometown", "Year of birth", "Year of death", if it's not available, you must select the "unknown" button or it will report an error of missing information.
### 4.2.9. fXoaTacGia interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/XoaTG.png)

Allows deleting authors in the database. Select the authors to delete in the list of displayed authors.
### 4.2.10. fLinhVuc interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/LinhVuc.png)

Allows adding new fields to the database. If you want to delete, select the fields to delete in the Menu below and press the delete button.
### 4.2.11. fLoaiSach interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/LoaiSach.png)

Allows adding new book categories to the database. If you want to delete, select the book categories to delete in the Menu below and press the delete button.
### 4.2.12. fNhaXuatBan interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/NXB.png)

Allows adding new publishers to the database. If you want to delete, select the publishers to delete in the Menu below and press the delete button.
### 4.2.13. fKho interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/Kho.png)
Gồm 2 phần:
- Phần trên: cho phép sửa số lượng sách có trong kho hoặc xóa luôn sách.
- Phần dưới: thêm số lượng cho đầu sách có trong kho.
### 4.2.14. fHoaDon interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/HoaDon.png)
Gồm 2 phần:
- Phần trên: hiển thị danh sách hóa đơn hiện có trong database cho phép xóa/sửa hóa đơn và xem chi tiết hóa đơn đó ở bảng kế bên.
- Phần dưới: thêm/sửa hóa đơn, thêm vật phẩm vô hóa đơn, yêu cầu nhập đầy đủ thông tin.
### 4.2.15. fThongKe interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/ThongKe.png)
Chọn khoảng ngày cần thống kê bán hàng, phần mềm sẽ hiển thị những hóa đơn trong khoảng ngày được chọn.
### 4.2.16. fBaoCao interface
![](https://github.com/hoainam2310/BookStore_Management/blob/main/Scene/BaoCao.png)
Xuất báo cáo chi tiết về số lượng bán đượccác loại sách, doanh thu và lợi nhuận trong khoảng ngày đã chọn ở màn hình fThongKe.
# 5. Design architecture
## 5.1. System architecture
![](https://github.com/hoainam2310/BookStore_Management/blob/main/layer.png)
| Thành phần | Diễn giải                         |
|------------|-----------------------------------|
| Client     | Ứng dụng tương tác với người dùng |
| Data       | Nơi chứa dữ liệu của hệ thống     |
## 5.2. Desribe in detail system architecture
![](https://github.com/hoainam2310/BookStore_Management/blob/main/folderview.png)
- Ứng dụng được thiết kế theo mô hình 2 lớp (được viết chung trong 1 project) gồm:
  - View xử lý giao diện và xử lý tác vụ.
  - DAO gọi các truy xuất từ csdl (SQL).
# 6. Coding conventions
## 6.1. Naming conventions
| Kiểu        | Mô tả           | Ví dụ        |
|-------------|-----------------|--------------|
| Pascal Case | Chữ cái đầu tiên trong từ định danh và chữ cái đầu tiên của mỗi từ nối theo sau phải được viết hoa. Sử dụng Pascal Case để đặt tên cho một tên có từ 3 ký tự trở lên | `CodingConv` |
| Camel Case  | Chữ cái đầu tiên trong từ định danh là chữ thường và chữ cái đầu tiên của mối từ nối theo sau phải được viết hoa          | `codingConv` |
| Uppercase   | Tất cả các ký tự trong từ định danh phải được viết hoa. Sử dụng quy tắc này đối với tên định danh có từ 2 ký tự trở xuống | `System.IO ` |
## 6.2. Conventions used when coding
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
## 6.3. Control prefixed
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
## 6.4. Source code distribution rules
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
# 7. Result
## 7.1. Development environment and Deployment environment
- Môi trường phát triển ứng dụng:
  - Hệ điều hành: Microsoft Windows 10
  - Hệ quản trị cơ sở dữ liệu: Microsoft SQL Server
  - Công cụ phân tích thiết kế: Visual Studio 2019
  - Công cụ xây dựng ứng dụng: Visual Studio 2019
- Môi trường triển khai ứng dụng:
  - Hệ điều hành: Microsoft Windows
  - Cần cài đặt .Net Framework 4.0 hoặc cao hơn
  - Để chương trình hoạt động cần có đủ các dll trong folder dll
## 7.2. Result
- Chương trình đã được hoàn thiện hầu hết các chức năng, nhưng vẫn có những chức năng chưa được hoàn thiện như: Thêm tài khoản, Xuất file báo cáo dạng PDF hoặc Excel.
## 7.3. Development
- Hoàn thiện các chức năng và giao diện chưa hoàn tất.
- Cải thiện hiệu năng của chương trình để phù hợp với thực tiễn.
- Bổ sung các chức năng liên quan đến CSDL: backup/restore.
- Bổ sung phân quyền tài khoản cho các chức năng của phần mềm.
