1)  **Coding Convention**: dựa theo chuẩn PSR-2 và PSR-4 (Laravel 6.x)

    a.  **Một số quy tắc**

-   Sau phần khai báo namespace của class phải chừa một dòng trống

-   Dùng 4 phím space để thụt dòng

-   Dấu { mở cho class hoặc hàm phải nằm ở một dòng mới kế dòng khai báo
    > tên cho chúng; dấu } đóng cho class hoặc phải nằm ở một dòng riêng
    > nằm ở cuối cùng của chúng

-   Tính đóng mở (*public*, *protected*, *private*) phải được khai báo ở
    > tất cả hàm, phương thức; từ khóa *abstract* hay *final* phải nằm
    > trước thuộc tính đóng mở; từ khóa *static* phải nằm sau thuộc tính
    > đóng mở

-   Các từ khóa cho cấu trúc điều khiển phải có dấu cách phía sau nó

-   Dấu { mở cho cấu trúc điều khiển phải nằm cùng một dòng với dòng
    > khai báo và cách nhau một khoảng trắng; dấu } đóng cho cấu trúc
    > điều khiển phải nằm ở dòng riêng kết thúc cho câu trúc điều khiển
    > đó

-   Phía sau dấu ( mở cho cấu trúc điều khiển không được có space ở phía
    > sau; dấu ) đóng cho cấu trúc điều khiển không được có dấu cách
    > phía trước

-   Tên class phải viết hoa chữ cái đầu tiên của mỗi từ

-   Tên các hàm cũng phải viết hoa chữ cái đầu tiên của mỗi từ trừ từ
    > đầu tiên

-   Tên hàm phải được viết in hoa toàn bộ và được phân cách bởi dấu gạch
    > dưới \_

-   Tên các thuộc tính (biến) có thể đặt thoải mái nhưng phải theo quy
    > tắc chung, nhất quán

-   \...

    a.  **Công cụ kiểm tra**

        i.  PHP Codesniffer

```{=html}
<!-- -->
```
-   Chèn dòng này vào mục require-dev của file composer.json của
    > project: \"squizlabs/php\_codesniffer\": \"3.\*\"

-   Để checking coding convention theo chuẩn PSR2 với một file hay thư
    > mục nhất định trong project, chúng ta chạy lệnh ./vendor/bin/phpcs
    > \--standard=PSR2 path/to/file/or/directory

-   Để tool tự động sửa các lỗi sai chuẩn với file hay thư mục, chạy
    > lệnh ./vendor/bin/phpcbf \--standard=PSR2
    > path/to/file/or/directory

2)  **Research folder "vendor" in project Laravel:**

-   Là thư mục chứa các thư viện composer mà project đã cài đặt, mỗi thư
    > mục tương ứng cho một dependency

-   Các thư mục được cài đặt và nằm trong thư mục *vendor* phải được
    > khai báo trong file composer.json nằm ở thư mục gốc của project

    -   File composer.json là file có nhiệm vụ quản lý các gói
        > dependency

    -   Mặc định file này sẽ được tự động tạo khi tạo mới một ứng dụng
        > laravel, nếu không có thể tạo mới bằng cách chạy lệnh composer
        > init trên terminal và điền một số thông tin project cũng như
        > các dependency cần sử dụng để tạo

    -   Các dependency nằm trong mục *require* và *require-dev* sẽ được
        > tải về và lưu trữ trong thư mục vendor

        -   *require* là những dependency bắt buộc phải có để project có
            > thể chạy

        -   *require-dev* là những dependency cần thiết để tạo môi
            > trường chạy project nhưng không bắt buộc

        -   Khi thêm mới một dependency vào, để project có thể cập nhật
            sự thay đổi, cần chạy lệnh composer update
