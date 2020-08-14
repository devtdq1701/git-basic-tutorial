**Tài liệu hướng dẫn sử dụng git cơ bản by Trần Đăng Quang**

---

> Mục lục

- [1. Tổng quan về git và github](#tongquan)
- [2. Một số thuật ngữ cần biết](#thuatngu)
- [3. Các thao tác cơ bản với git và github](#thaotac)

---

<a href="tongquan"></a>

## 1. Tổng quan về git và github

### 1.1. Git

- `Git` là tên gọi của một `hệ thống quản lý phiên bản phân tán` (`Distributed Verson Control System - DVCS`), một trong những hệ thống quản lý phiên bản phân tán phổ biến nhất hiện nay.
- `DVCS` giúp mỗi PC có thể `lưu trữ` nhiều phiên bản khác nhau của một bộ source code đã được nhân bản (`clone`) từ 1 kho chứa mã nguồn (`repository`), các thay đổi trên mã nguồn sẽ được `commit` rồi `push` lên server nơi đặt kho chứa chính (`remote repository`). Các PC khác (có quyền truy cập) cũng có thể `clone` lại mã nguồn từ kho chứa để lấy phiên bản mới nhất. Khái niệm này gọi là `working tree`.
  ![](./ghichep-Git-master/images/git-overview-1.png)
  ![](./ghichep-Git-master/images/git-overview-fb-1.png)

- `Git` tối ưu hơn các hệ thống quản lý code thống thường vì có khả năng `branch`, hỗ trợ tốt cho teamwork, vì những việc như phân chia task, tổng hợp code trở nên dễ dàng hơn nhiều.

**Tính chất của git:**

- An toàn, nhanh chóng, dễ sử dụng
- Giúp cho việc làm việc nhóm đơn giản = cách `merge` các `branch`
- Git giống như 1 chuẩn quản lý mã nguồn, giống như `SVN`
- Có nhiều trang hỗ trợ git k chỉ riêng github, như bitbucket

### 1.2. Github

- Github là một trang web, nơi bạn có thể lưu trữ code của mình trên đó.
- Sự kết hợp hoàn hảo giữa git và github mang lại sự thuận tiện: bạn có thể code của mỉnh ở mọi nơi, k sợ bị ghi đè, bị mất dữ liệu, có thể trở về thời điểm bất kỳ mà bạn thay đổi code

<a href="thuatngu"></a>

## 2. Một số thuật ngữ cần biết

- Repository (kho): là thư mục. Thư mục trên github.com gọi là remote (xa) repository (kho), còn ở máy tính là local repository.
- Branch (nhánh): ví dụ t làm 1 phần trên 1 nhánh, m rẽ sang nhánh khác làm chức năng khác, sau này hộp lại (merge)
- Remote (máy chủ): khỏi giải thích, lát ví dụ
- add (thêm): sau khi làm gì đó thay đổi thì add (thêm) cái thay đổi đó vào
- commit: chốt thay đổi
- pull (kéo về): lấy code của thằng làm chung đã push (đẩy) lên.
  Pull từ từ branch nào về branch hiện tại cũng được, nếu pull từ branch khác thì sẽ có "Merge" xảy ra, còn pull từ cũng branch thì là như update code base.Khi mình làm thay đổi dưới local trùng với chỗ người nào đó đã sửa và push lên (nhưng mình chưa pull về trước đó), thì khi pull về sẽ có "conflict"."Conflict" nghĩa là "đụng độ". Khi code pull về bị conflict, cần phải "Resolve conflict" bằng cách chọn thay đổi nào được giữ lại và thay đổi nào sẽ xóa đi hoặc giữ lại cả 2 và chỉnh sữa cho tụi nó hoạt động.
- push (đẩy): đưa code lên remote repository, nghĩa là đẩy lên cho tụi kia kéo về
- Collaborators: làm việc nhóm với git như nào:
- ai tạo repos thì vào đây:
  `https://github.com/<tên_tài_khoản>/<tên_repos>/settings/collaboration`
- gõ email github thành viên vào, thằng được mời làm chung đồng ý thì làm thôi.

<a href="thaotac"></a>

## 3. Thao tác với git và github

- Tạo 1 remote trên github
- Tạo 1 thư mục để chứa code dưới máy tính. Chuột phải >git bash here. Khởi tạo, gõ: git init
- Liên kết với remote = lệnh: git remote add origin <link remote>
- Sau khi liên kết, để kéo hết nội dung trên remote về: git pull origin master
- Khi có các thay đổi ở local repo:
- kiểm tra trạng thái: git status
  -add: git add <tên file> hoặc git add \* để thêm tất
  -commit: git commit -m "ghi chú về commit" để thêm comment
  -git remote add origin <link remote>
  -push: git push -u origin master
- Khi có ai đó push gì mới, kéo về tại thư mục đã khởi tạo (git init): git pull origin master
- Clone: clone repo của ng khác: git clone <link repo>
- Luyện tập bằng cách tạo repo trống trên github

> Lưu ý: Đây chỉ là 1 số thao tác cơ bản. Ngoài ra còn có git gui có giao diện trực quan, dùng chuột thay vì dùng lệnh :v

**update-git:**

- git update-git-for-windows
