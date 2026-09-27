# Flutter Learning — 48 tuần từ số 0 tới Junior Flutter Developer

Repo này là toàn bộ quá trình học Flutter của tôi, bắt đầu **25/09/2026**, mục tiêu đi phỏng vấn từ **tháng 9/2027**, nhịp **10–12 giờ/tuần**.

**Bảng theo dõi tiến độ:** https://claude.ai/artifact/6S563worA1E2M9g2m5QkyQ

| | |
|---|---|
| Giai đoạn hiện tại | 1 / 8 — Nền tảng & Dart |
| Tuần hiện tại | 1 / 48 |
| Dự án đã xong | 0 / 3 |

---

## Môi trường

Đã cài và `flutter doctor` không lỗi (kiểm tra 25/09/2026):

| | |
|---|---|
| Flutter | 3.44.6 · channel stable |
| Dart | 3.12.2 |
| Android | SDK 36.0.0 |
| iOS | Xcode 26.2 |
| Máy | macOS 26.6.2 · arm64 |

Kiểm tra lại bất cứ lúc nào:

```bash
flutter doctor -v
```

---

## Cấu trúc

```
01-dart/                 Tuần 1–6   Git, Dart, OOP, async, test
02-flutter-ui/           Tuần 7–12  Widget, layout, form, list, navigation
03-state-architecture/   Tuần 13–18 Provider, BLoC, Riverpod, Clean Architecture
04-data/                 Tuần 19–24 Dio, auth, local storage, offline, Firebase
05-quality/              Tuần 25–30 Test, CI/CD, flavor, quy trình Git
06-advanced-native/      Tuần 31–36 Animation, performance, platform channel, i18n
07-capstone/             Tuần 37–42 Dự án tốt nghiệp, phát hành thật
08-job-hunt/             Tuần 43–48 CV, ôn phỏng vấn, thuật toán, apply
projects/                3 dự án portfolio
notes/                   Ghi chú mỗi tuần — week-01.md, week-02.md, ...
```

Mỗi giai đoạn có `README.md` riêng liệt kê 6 tuần và kết quả cần đạt. Thư mục tuần chỉ tạo khi bắt đầu tuần đó, không tạo trước 48 thư mục rỗng.

---

## Quy ước

**Commit message viết bằng tiếng Anh**, theo [Conventional Commits](https://www.conventionalcommits.org). Lịch sử Git của repo này sẽ được recruiter và tech lead đọc, trong đó có người nước ngoài — và tiếng Anh là quy ước mặc định ở gần như mọi team. Đây cũng là chủ đề được đào sâu ở tuần 27.

```
<type>(<scope>): <mô tả ngắn, thể mệnh lệnh, không dấu chấm cuối>
```

| Type | Dùng khi |
|---|---|
| `feat` | thêm tính năng |
| `fix` | sửa lỗi |
| `refactor` | đổi code, không đổi hành vi |
| `perf` | tối ưu hiệu năng |
| `test` | thêm hoặc sửa test |
| `docs` | README, ghi chú, comment |
| `style` | format, lint, không đổi logic |
| `chore` | cấu hình, dependency, dọn dẹp |
| `ci` | pipeline, workflow |

`scope` là nơi bị ảnh hưởng — tuần đang học, hoặc tên feature:

```
docs: add 48-week roadmap structure and week 1 guide
feat(week-03): read and write expense data as JSON
refactor(week-04): extract Transaction into its own class
test(week-06): cover quiz scoring logic
fix(expense-tracker): keep VND format when editing an amount
chore(ci): cache pub dependencies in GitHub Actions
```

Ba điều dễ sai:

- **Dùng thể mệnh lệnh**, không phải quá khứ: `add validation`, không phải `added validation`. Đọc là "commit này sẽ ... ".
- **Một commit = một thay đổi có nghĩa.** Nếu phải viết `and` trong mô tả thì nên tách thành hai commit.
- **Mô tả cái gì thay đổi và vì sao**, không phải thay đổi ở đâu — file nào thì `git diff` đã nói rồi.

Ghi chú trong `notes/` vẫn viết bằng tiếng Việt: mục đích ở đó là hiểu sâu, không phải luyện tiếng Anh.

**Ba quy tắc không phá**

1. Commit mỗi ngày có học — kể cả chỉ là một file ghi chú.
2. Không xem tiếp khi chưa gõ. Mỗi khái niệm phải có một file code của riêng mình.
3. Không nhảy cóc giai đoạn. Bỏ Dart để nhảy vào widget là lý do phổ biến nhất khiến người học tắc ở tháng thứ tư.

**Ghi chú mỗi tuần.** Cuối mỗi tuần copy `notes/_template.md` thành `notes/week-XX.md` và điền. Viết bằng lời của mình, không copy tài liệu — đây chính là phần trả lời phỏng vấn ở tuần 44–45.

---

## Chia thời gian một tuần (11 giờ)

| Khối | Giờ | Làm gì |
|---|---|---|
| Học lý thuyết | 3 | Đọc docs, xem video đúng chủ đề của tuần |
| Code theo bài | 3 | Gõ lại ví dụ cho tới khi hiểu vì sao nó chạy |
| Dự án | 4 | Áp kiến thức tuần này vào dự án đang chạy — không được cắt |
| Ôn & viết | 1 | Viết `notes/week-XX.md`, đọc 1 bài tiếng Anh về Flutter |

Khi bị trễ, cắt theo thứ tự: bài tập nhỏ → phần đọc thêm → chiều sâu chủ đề. Không bao giờ cắt phần dự án và phần test.
