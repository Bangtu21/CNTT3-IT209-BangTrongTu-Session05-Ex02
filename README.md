Session05-Ex02
## 1. Tạo lịch sử commit
Tạo 4 commit trên nhánh `master`:

* `feat: khoi tao module auth`
* `fix auth`
* `adds utility functions`
* `add temp file for debug`

## 2. Thực hiện Interactive Rebase
Do commit đầu tiên là root commit nên sử dụng:

git rebase -i --root

Trong giao diện Interactive Rebase, cấu hình:

* Commit 1: `pick`
* Commit 2: `squash`
* Commit 3: `squash`
* Commit 4: `drop`

Ba commit đầu được gộp thành một commit duy nhất, còn commit chứa `temp.txt` được loại bỏ hoàn toàn.

## 3. Đổi thông điệp commit

Sau khi squash, Git mở trình soạn thảo để chỉnh sửa commit message.

Thông điệp mới:

feat: hoan thien module authentication

## 4. Kiểm tra kết quả

Sử dụng:

git log --oneline

Kết quả:

bd7a398 feat: hoan thien module authentication

Lịch sử chỉ còn một commit duy nhất, không còn các commit `fix auth`, `adds utility functions` và `add temp file for debug`.