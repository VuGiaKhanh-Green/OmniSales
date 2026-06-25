# I. Giới thiệu dự án

OmniSales là một hệ thống Sàn thương mại điện tử nhiều người bán (Multi-vendor E-commerce), kết nối mạnh mẽ giữa Khách hàng, người bán (Vendor) và Quản trị sàn (Admin). Dự án được xây dựng theo kiến trúc 3 tầng trên nền tảng ASP.NET Core MVC (C#), sử dụng Entity Framework Core và MS SQL cho các tác vụ quản trị cơ sở dữ liệu, kết hợp cùng giao diện người dùng mượt mà được xây dựng từ HTML, CSS, JavaScript và Bootstrap. Tính thực tiễn của dự án được thể hiện qua việc :

  1. Ứng dụng ASP.NET Core Identity để phân quyền người dùng
  2. Tương tác với khách hàng của người bán thông qua đánh giá đơn hàng và nhắn tin trực tuyến 
  3. Chuẩn hóa toàn bộ quy trình mua bán lẫn quản lý của 1 sàn thương mại điện tử (quản lý sản phẩm, thiết lập Voucher,thanh toán, quản lý và xử lý đơn hàng), tạo nên một hệ thống có tính ổn định và có khả năng mở rộng cao.
  4. Hệ thống Cấu hình Động, Quản trị sàn có thể thay đổi các thông số vận hành (như % hoa hồng sàn, phí vận chuyển mặc định, số ngày cho phép hoàn trả) ngay trên giao diện Web
  5. Tích hợp SignalR để xử lý các tính năng thời gian thực như Chat trực tiếp và thông báo.

# II. Hướng dẫn cài đặt

  Bước 1: Tải và cài đặt Visual Studio : https://visualstudio.microsoft.com/fr/thank-you-downloading-visual-studio/?sku=Community&channel=Stable&version=VS18&source=VSLandingPage&cid=2500&passive=false
  
  Bước 2: Chọn các ToolSet của Visual Studio:

  ![alt]


