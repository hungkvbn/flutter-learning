# Tuần 1 — Môi trường làm việc & Git

**~11 giờ** · Kết quả: repo GitHub public có README mô tả lộ trình.

Tuần này không viết Dart. Mục tiêu là làm chủ hai công cụ sẽ dùng mỗi ngày trong 47 tuần tới: terminal và Git. Bỏ qua tuần này thì tuần 27 (Git & làm việc nhóm) sẽ rất chật vật, và phỏng vấn outsource gần như chắc chắn hỏi về quy trình Git.

## Việc cần làm

### 1. Terminal (2 giờ)
- [ ] `pwd`, `cd`, `ls -la`, `mkdir`, `rm -r`, `cp`, `mv`, `cat`, `open .`
- [ ] Tìm kiếm: `grep -rn "chuỗi cần tìm" .`, `find . -name "*.dart"`
- [ ] Pipe và chuyển hướng: `ls | grep dart`, `flutter doctor > doctor.txt`
- [ ] Tự đặt 3 alias trong `~/.zshrc` (ví dụ `alias fd="flutter doctor"`)

### 2. Git cơ bản (4 giờ)
- [ ] Hiểu 3 khu vực: working directory → staging area → repository
- [ ] `git status`, `git add`, `git commit -m`, `git log --oneline --graph`
- [ ] `git diff` và `git diff --staged` — khác nhau ở đâu?
- [ ] Hoàn tác: `git restore <file>`, `git restore --staged <file>`, `git commit --amend`
- [ ] Nhánh: `git branch`, `git switch -c feat/test`, `git merge`, xoá nhánh
- [ ] Tự tạo một conflict rồi tự giải quyết — làm ít nhất 2 lần cho quen

### 3. GitHub (3 giờ)
- [ ] Tạo SSH key và thêm vào GitHub: `ssh-keygen -t ed25519 -C "hungkvbn@gmail.com"`
- [ ] Kiểm tra: `ssh -T git@github.com`
- [ ] Đẩy repo này lên GitHub, đặt public
- [ ] `git push`, `git pull`, `git clone` — thử clone lại repo của mình về thư mục khác
- [ ] Tạo một Pull Request từ nhánh phụ vào `main`, tự review, rồi merge

### 4. Markdown & ghi chú (2 giờ)
- [ ] Heading, list, bảng, code block, link, ảnh
- [ ] Viết `notes/week-01.md` theo template trong `notes/_template.md`
- [ ] Bổ sung README gốc: thêm phần "Nhật ký" ghi ngày bắt đầu

## Câu hỏi tự kiểm tra cuối tuần

Trả lời thành tiếng, không nhìn tài liệu:

1. Staging area để làm gì? Vì sao Git không commit thẳng từ working directory?
2. `git restore --staged file.dart` khác `git restore file.dart` ở chỗ nào?
3. Khi nào nên tạo nhánh mới thay vì commit thẳng vào `main`?
4. `.gitignore` hoạt động thế nào với file đã được commit từ trước?
5. Vì sao không bao giờ được commit file `.env` hay keystore?

## Cạm bẫy thường gặp

- **Commit message vô nghĩa** (`update`, `fix bug`, `asdf`). Từ tuần này đã dùng Conventional Commits — xem quy ước ở README gốc.
- **Commit quá to.** Một commit = một thay đổi có nghĩa. Commit 40 file cùng lúc thì không ai review nổi, kể cả chính mình sau 3 tháng.
- **Sợ nhánh.** Nhánh trong Git rất rẻ. Tạo nhánh cho mọi thứ.
