# I. Giới thiệu dự án

OmniSales là một hệ thống Sàn thương mại điện tử nhiều người bán (Multi-vendor E-commerce), kết nối mạnh mẽ giữa Khách hàng, người bán (Vendor) và Quản trị sàn (Admin). Dự án được xây dựng theo kiến trúc 3 tầng trên nền tảng ASP.NET Core MVC (C#), sử dụng Entity Framework Core và MS SQL cho các tác vụ quản trị cơ sở dữ liệu, kết hợp cùng giao diện người dùng mượt mà được xây dựng từ HTML, CSS, JavaScript và Bootstrap. Tính thực tiễn của dự án được thể hiện qua việc :

  1. Ứng dụng ASP.NET Core Identity để phân quyền người dùng
  2. Tương tác với khách hàng của người bán thông qua đánh giá đơn hàng và nhắn tin trực tuyến 
  3. Chuẩn hóa toàn bộ quy trình mua bán lẫn quản lý của 1 sàn thương mại điện tử (quản lý sản phẩm, thiết lập Voucher,thanh toán, quản lý và xử lý đơn hàng), tạo nên một hệ thống có tính ổn định và có khả năng mở rộng cao.
  4. Hệ thống Cấu hình Động, Quản trị sàn có thể thay đổi các thông số vận hành (như % hoa hồng sàn, phí vận chuyển mặc định, số ngày cho phép hoàn trả) ngay trên giao diện Web
  5. Tích hợp SignalR để xử lý các tính năng thời gian thực như Chat trực tiếp và thông báo.

# II. Hướng dẫn cài đặt 
   
    Do dự án này sử dụng phiên bản Entity Framework Core chỉ tương thích với biên bản .NET 8.0 nên phải tải 
    Microsoft.AspNetCore.App phiên bản 8.0.0 (x64)

  
  Bước 1: Tải môi trường asp.net core 8.0:  https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-aspnetcore-8.0.28-windows-x64-installer?cid=getdotnetcore

    Mở và cài đặt môi trường asp.net core 8.0
  <img width="995" height="492" alt="image" src="https://github.com/user-attachments/assets/e302b8d1-c1d2-4344-9f5f-70109f815a0c" />
  <img width="569" height="338" alt="image" src="https://github.com/user-attachments/assets/1fd21742-8f29-4b72-85fa-87c7feff3020" />
  <img width="567" height="335" alt="image" src="https://github.com/user-attachments/assets/59495226-f9a0-4db2-8e66-953ea8473044" />


  Bước 2: Tải Visual Studio : https://visualstudio.microsoft.com/fr/thank-you-downloading-visual-studio/?sku=Community&channel=Stable&version=VS18&source=VSLandingPage&cid=2500&passive=false
  
  Bước 3: Chọn các ToolSet của Visual Studio và bấm install để cài đặt

  ![alt](https://private-user-images.githubusercontent.com/178351088/612946146-5367ec32-de83-42ed-92dc-de10c23d66a6.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODIzNzcxNjYsIm5iZiI6MTc4MjM3Njg2NiwicGF0aCI6Ii8xNzgzNTEwODgvNjEyOTQ2MTQ2LTUzNjdlYzMyLWRlODMtNDJlZC05MmRjLWRlMTBjMjNkNjZhNi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwNjI1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDYyNVQwODQxMDZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1mYjlkNmI4NGNkZmM2MGNjNTQ4YjA3OTY3N2NmYWI3ZWM4MjQ5ZDc0NTY5ODYzMTg4N2JhZTY5MTY1ZDc1ZDg4JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZyZXNwb25zZS1jb250ZW50LXR5cGU9aW1hZ2UlMkZwbmcifQ.kqL7ftq3nFGw1MlWQlu1OFXsGJGpN9NPRWiCNFqXQPg)

![alt](https://private-user-images.githubusercontent.com/178351088/612946145-25a11f04-b795-47cd-8bc0-5705f0202d47.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODIzNzcxNjYsIm5iZiI6MTc4MjM3Njg2NiwicGF0aCI6Ii8xNzgzNTEwODgvNjEyOTQ2MTQ1LTI1YTExZjA0LWI3OTUtNDdjZC04YmMwLTU3MDVmMDIwMmQ0Ny5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwNjI1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDYyNVQwODQxMDZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1kNWU4NjYxODk2NmVlNTE3NjA4MjUwYTFlOWEzYjUxNzE3MTgxYzFmMjc4NGQ4ODk3MzM2ODM5NWRhNDA0NGU1JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZyZXNwb25zZS1jb250ZW50LXR5cGU9aW1hZ2UlMkZwbmcifQ.MbjInJSzCl7nyGGs7Ch7alwvuC1Y-7v89IpcaK0l3W8)

![alt](https://private-user-images.githubusercontent.com/178351088/612946138-27d6f296-dd95-4f3a-8114-98be1ce81e59.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODIzNzcxNjYsIm5iZiI6MTc4MjM3Njg2NiwicGF0aCI6Ii8xNzgzNTEwODgvNjEyOTQ2MTM4LTI3ZDZmMjk2LWRkOTUtNGYzYS04MTE0LTk4YmUxY2U4MWU1OS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwNjI1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDYyNVQwODQxMDZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iMTc5ZTE1OTAwNWIxOGI5YjQ2MGIzNzM0ZjAxN2Q4NTVmN2E0ZWU1ZGQ4NTcwYTc1ZTVmMDRlZmEwZTk0MGFlJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZyZXNwb25zZS1jb250ZW50LXR5cGU9aW1hZ2UlMkZwbmcifQ.DrqmVQkh_3u1lVkfdsqjIV1Vn5fsW-iZS9TyzAMzqn0)

Bước 4: Tải mã nguồn (source code ) của dự án- chính là Omnisales.rar nằm ở phần SourceCode của repository này

![alt](https://private-user-images.githubusercontent.com/178351088/612946137-e21419bb-e36f-4e2e-ba74-4ece35efd49c.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODIzNzcxNjYsIm5iZiI6MTc4MjM3Njg2NiwicGF0aCI6Ii8xNzgzNTEwODgvNjEyOTQ2MTM3LWUyMTQxOWJiLWUzNmYtNGUyZS1iYTc0LTRlY2UzNWVmZDQ5Yy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwNjI1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDYyNVQwODQxMDZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1kMzMzNTNjNjNmZjMyOTYyYTQ2NjY0YTM0YjQ1NmNmMjMxNzgxZjQ3ODVlOWM5ZTUyYTc2YzE5YjkwMjE3MjBhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZyZXNwb25zZS1jb250ZW50LXR5cGU9aW1hZ2UlMkZwbmcifQ.O_xUUDgYLx0mgeIZYYI7kElcpYnEQxhybU2gMm7SsQg)

![alt](https://private-user-images.githubusercontent.com/178351088/612946136-5097ef08-3e4b-45c5-babd-4a7ead60220b.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODIzNzc0OTYsIm5iZiI6MTc4MjM3NzE5NiwicGF0aCI6Ii8xNzgzNTEwODgvNjEyOTQ2MTM2LTUwOTdlZjA4LTNlNGItNDVjNS1iYWJkLTRhN2VhZDYwMjIwYi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwNjI1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDYyNVQwODQ2MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iZTc4NzIyZjMzNGExYTRjNzNiMzRmM2YyN2NiMTA5OWEwNjBhMGRhM2MyYmZmNDE2NjU2MmIwYzczZmJmZTEzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZyZXNwb25zZS1jb250ZW50LXR5cGU9aW1hZ2UlMkZwbmcifQ.CsXb82AaupO_sAEL2OBFitxsLjv_g_YxraZvVJNQ8Yo)

Bước 5: Giải nén

![alt](https://private-user-images.githubusercontent.com/178351088/612946144-c698935f-8617-4248-a43b-8bc2590c7ac1.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODIzNzc0OTYsIm5iZiI6MTc4MjM3NzE5NiwicGF0aCI6Ii8xNzgzNTEwODgvNjEyOTQ2MTQ0LWM2OTg5MzVmLTg2MTctNDI0OC1hNDNiLThiYzI1OTBjN2FjMS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwNjI1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDYyNVQwODQ2MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05MTc1MzY2ZTJmNmI5NzZiNjZiZTIzNWEwNjA3NjkwZDM4ZDJiZGQ1NzgyZmUxYzg5YTIxMTkyYWQyMjQzN2UxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZyZXNwb25zZS1jb250ZW50LXR5cGU9aW1hZ2UlMkZwbmcifQ.viwkK-iMiPZrw0V0J4ZayAM57lIzSm3jd7nkBIjqG8Y)

<img width="1124" height="521" alt="image" src="https://github.com/user-attachments/assets/2c384e37-16a8-412e-bb34-3f4fdc06141f" />

Bước 6: Mở project bằng Visual Studio bằng cách mở thư mục vừa giải nén rồi chạy Solution

<img width="1118" height="447" alt="image" src="https://github.com/user-attachments/assets/9b64ff4a-c590-4175-822a-229204d1107b" />

Bước 7: Tải và cài đặt lại các thư viện

    Click chuột phải vào "Solution 'OmniSales'" rồi chọn "Build Solution"
<img width="1920" height="1010" alt="image" src="https://github.com/user-attachments/assets/8fa700f6-6b67-45d5-8966-2ed6aabc1007" />

<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/5e627f47-dc6f-4bf6-b59e-8a208545ec95" />

Bước 8: Cập nhật dữ liệu

    Nhìn lên thanh menu trên cùng, chọn Tools -> NuGet Package Manager -> Package Manager Console. 
    Một màn hình gõ lệnh màu đen sẽ hiện ra ở dưới đáy màn hình
<img width="1920" height="1039" alt="image" src="https://github.com/user-attachments/assets/ebb9f7db-97c2-4256-b0ad-f0abf9f8deb4" />

    Ở màn hình gõ lệnh đó, nhìn chỗ có chữ Default project:,bấm xổ xuống và chọn đúng chữ OmniSales.Infrastructure
<img width="1920" height="1015" alt="image" src="https://github.com/user-attachments/assets/d11af88f-f5d9-48a2-8a25-150b9f30dbb7" />

    Gõ lệnh "Update-Database"
<img width="1920" height="1009" alt="image" src="https://github.com/user-attachments/assets/0f48a364-4275-497d-96b2-c5eb78936779" />

    Chờ chạy xong báo chữ "Done" là thành công
<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/1778798e-92f9-48f9-81ac-f6dd87ad31cd" />


Bước 8.1: Tải data mẫu (optional-không bắt buộc )

    Tải data mẫu: chính là OmnisalesDb.bank nằm ở phần SourceCode của repository này
<img width="1920" height="956" alt="image" src="https://github.com/user-attachments/assets/e066996f-1c4b-4d14-ae18-9fb34fac2378" />

    Click chuột phải vào file vừa tải về, chọn properties -> General để xem vị trí file 
    (vị trí của mình là C:\Users\Administrator\Downloads )
<img width="1096" height="538" alt="image" src="https://github.com/user-attachments/assets/d42372e8-847b-45a2-b1df-dc7cad4edc29" />
<img width="1118" height="607" alt="image" src="https://github.com/user-attachments/assets/26633cb6-b899-4043-b56c-ff0b9bb9de9c" />

Bước 8.2: Tải dữ liệu lên database

    Nhìn lên thanh menu trên cùng, chọn View -> SQL Server Object Explorer 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/04eb0a9f-4057-437e-84b1-2e637179b583" />

    Một cửa sổ nhỏ hiện ra bên trái,bấm vào SQL Server để xổ ra 
    
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7aae8fac-a972-48ea-8a09-b42f77c7aa8f" />

    Chọn (localdb)\MSSQLLocalDB -> Databases
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c978f39e-16a2-4049-8eca-5d3a255bbff1" />

    Chuột phải vào OmniSalesDb -> Chọn New Query
<img width="354" height="946" alt="image" src="https://github.com/user-attachments/assets/1fbfa4bb-7ce3-46de-99c3-ca91913a2611" />

    Nhập nội dung truy vấn như sau :
  ```sql
USE master;
ALTER DATABASE OmniSalesDb SET SINGLE_USER WITH ROLLBACK IMMEDIATE;

RESTORE DATABASE OmniSalesDb
FROM DISK = 'C:\Users\Administrator\Downloads\OmniSalesDb.bak' /* thay bằng địa chỉ file bak ở máy hiện tại - bước 8.1 */
WITH REPLACE,
MOVE 'OmniSalesDb' TO 'C:\Users\Public\OmniSalesDb.mdf', /* ép vào thư mục public mà luôn được cấp quyền truy cập, ở đây của mình là 'C:\Users\Public */
MOVE 'OmniSalesDb_log' TO 'C:\Users\Public\OmniSalesDb_log.ldf';  /* ép vào thư mục public mà luôn được cấp quyền truy cập, ở đây của mình là 'C:\Users\Public */

ALTER DATABASE OmniSalesDb SET MULTI_USER;
  ```
<img width="1920" height="1014" alt="image" src="https://github.com/user-attachments/assets/b798f555-662a-4ef0-9a77-fe1f2a18107f" />

    Chạy câu truy vấn
<img width="1920" height="1041" alt="image" src="https://github.com/user-attachments/assets/2e3f7118-c558-4b65-81cf-4c18bc19b289" />

Bước 9: Chạy dự án bằng cách click vào OmniSales.Web ở phần solution. Chọn http và bấm F5 để chạy

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e8c2bfc4-6848-4cfc-b883-1d4a4c19605b" />

Tài khoản Admin:
admin@omnisales.com

Mật khẩu Admin:
Admin@123

Tài khoản Vendor:
vendor@omnisales.com

Mật khẩu Vendor:
Vendor@123

  Chú ý: Hệ thống hỗ trợ chạy đa vai trò đồng thời trên cùng một địa chỉ (cổng). Nên khi chạy được thành công, địa chỉ (cổng) sẽ xuất hiện ở phần đường dẫn trang web. Muốn thử các vai trò khác (bật nhiều tab để truy cập trang web) thì phải dùng đúng địa chỉ (cổng ) xuất hiện khi chạy thành công ở trên
















