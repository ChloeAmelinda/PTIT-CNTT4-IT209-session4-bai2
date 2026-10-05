# Bài 2: Kết hợp cập nhật từ main và feature-update

## Mục tiêu

Thực hành tạo nhánh, chuyển nhánh, tạo Merge Conflict và giải quyết
xung đột thủ công bằng trình soạn thảo văn bản.

## Các bước thực hiện

1. Khởi tạo repository Git với nhánh chính main.
2. Tạo homework/session_04/ex2/README.md và commit nội dung ban đầu.
3. Tạo nhánh feature-update từ main.
4. Sửa dòng tiêu đề README.md trên feature-update và commit.
5. Chuyển về main, sửa cùng dòng tiêu đề thành nội dung khác và commit.
6. Chạy git merge feature-update trên main.
7. Git báo xung đột vì hai nhánh cùng sửa một dòng.
8. Mở README.md bằng Notepad và đọc nội dung của hai nhánh.
9. Sửa tiêu đề thành nội dung kết hợp từ main và feature-update.
10. Xóa thủ công toàn bộ các dòng đánh dấu xung đột của Git.
11. Lưu file, chạy git add và git commit để hoàn thành gộp nhánh.
12. Kiểm tra lịch sử bằng git log --graph --oneline.

## Giải thích 3-Way Merge

Git sử dụng ba phiên bản để thực hiện gộp nhánh:

- Base: phiên bản tại commit tổ tiên chung gần nhất của hai nhánh.
- Ours: phiên bản của nhánh hiện tại main.
- Theirs: phiên bản của nhánh feature-update được gộp vào.

Trong bài tập, main và feature-update cùng sửa dòng tiêu đề của
README.md thành hai nội dung khác nhau so với phiên bản chung.
Git không thể tự chọn nội dung phù hợp nên yêu cầu xử lý thủ công.

Sau khi giải quyết xung đột, merge commit có hai commit cha:
commit đầu nhánh main và commit đầu nhánh feature-update trước khi gộp.

## Kết quả

- Đã giải quyết xung đột thủ công.
- File README.md không còn các dấu đánh dấu xung đột.
- Đã gộp feature-update vào main bằng một merge commit có hai commit cha.

## Minh chứng lịch sử commit

![Đồ thị lịch sử commit](git-log.png)