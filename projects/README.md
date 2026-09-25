# Ba dự án portfolio

Nhà tuyển dụng đọc code, không đọc số lượng. Ba dự án làm tới nơi tới chốn mạnh hơn mười app clone bỏ dở.

Mỗi dự án nằm trong thư mục con riêng ở đây, và khi hoàn thành thì **tách ra thành repo GitHub độc lập** để ghim lên profile.

| | Dự án | Tuần | Điểm chứng minh |
|---|---|---|---|
| 1 | Expense Tracker | 12 | Widget, layout, form, navigation, Material 3 |
| 2 | Movie / News App | 18–22 | Kiến trúc phân tầng, BLoC, Dio, cache offline, test |
| 3 | Capstone | 37–42 | Toàn bộ vòng đời sản phẩm: build → test → CI/CD → release |

Tiêu chí nghiệm thu chi tiết từng dự án nằm ở tab **Dự án** trong bảng theo dõi:
https://claude.ai/artifact/6S563worA1E2M9g2m5QkyQ

## Checklist chung trước khi coi một dự án là "xong"

- [ ] README có ảnh chụp màn hình, mô tả tính năng, hướng dẫn clone và chạy
- [ ] Không có secret, keystore hay `.env` trong lịch sử Git
- [ ] `flutter analyze` sạch, không warning
- [ ] `flutter test` xanh
- [ ] Chạy được trên cả Android và iOS
- [ ] Lịch sử commit đọc được, không có commit `update` hay `asdf`
