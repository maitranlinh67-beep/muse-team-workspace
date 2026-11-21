# Muse Team Workspace — Không Gian Làm Việc Chung (3 Bot Muse + DeepSeek API)

Thư mục này là **văn phòng dùng chung** cho 3 bot phối hợp với nhau theo cơ chế **Bảng việc chung (`TASKS.md`)**:

| Bot | Username Telegram | Vai trò | Prompt chuẩn |
| :--- | :--- | :--- | :--- |
| **Muse 1 (chính)** | `@Muse1cualinh_Bot` | Đầu não — phân việc, truyền Skill, gọi DeepSeek API khi cần, chốt cuối | `prompts/01_muse1_dau_nao.md` |
| **Muse 2 (Xoài Non)** | `@Muse2xoainon_BOT` | Thực thi — làm bản nháp, xử lý việc cùng Muse 1 & sửa theo kiểm duyệt | `prompts/02_muse2_thuc_thi.md` |
| **Muse 3 (Shop Xoai Non)** | `@Muse3cualinh_BOT` | Kiểm duyệt — soi lỗi logic, bắt lỗi bịa số liệu, đối chiếu Skill | `prompts/03_muse3_kiem_duyet.md` |
| **DeepSeek API** *(dưới tay Muse 1)* | `deepseek-chat` | Cố vấn logic, tính toán, trọng tài phá thế bế tắc, dự phòng | `prompts/04_deepseek_advisor.md` |

---

## Cấu trúc thư mục
- `TASKS.md` — Bảng việc chung đang chạy (giữ tối đa 10 task gần nhất để cả 3 bot đọc thật nhanh).
- `TASKS_ARCHIVE.md` — Lưu các task đã `DONE` cũ.
- `SOP-SKILLS.md` — Giáo trình & bộ quy tắc Skill rút gọn (≤500 chữ) do `@Muse1cualinh_Bot` biên soạn để dạy `@Muse2xoainon_BOT` và `@Muse3cualinh_BOT`.
- `prompts/` — Chứa sẵn System Prompt riêng cho từng bot (chỉ cần copy-dán).
- `outputs/` — Chứa file kết quả dài (>150 chữ) theo định dạng `T001_v1.md`, `T001_final.md`.

---

## 2 lệnh mẫu dùng ngay trong Group Telegram

### 1. Chạy 1 lần đầu (cho Muse 1 dạy Skill cho Muse 2 & Muse 3)
```text
@Muse1cualinh_Bot Hãy cập nhật file SOP-SKILLS.md trong thư mục chung (tối đa 500 chữ, gạch đầu dòng ngắn từ dữ liệu thật & kho Skill bạn đang có), gồm: (1) Thông tin cố định của dự án/shop, (2) 5 quy tắc Skill bắt buộc cho @Muse2xoainon_BOT, (3) 5 lỗi nghiêm trọng @Muse3cualinh_BOT phải soi. Xong báo group để 2 bot kia đọc và xác nhận 1 dòng.
```

### 2. Dùng hằng ngày khi giao việc mới
```text
@Muse1cualinh_Bot [VIỆC MỚI]
- Yêu cầu: <viết ngắn gọn cần làm gì>
- Dữ liệu thật: <giá, thông số, ghi chú thật — chưa có thì ghi "chưa có">
```
