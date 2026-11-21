@Muse1cualinh_Bot @Muse2xoainon_BOT @Muse3cualinh_BOT

HƯỚNG DẪN DÙNG CHUNG THƯ MỤC & CÁCH LÀM VIỆC CỦA ĐỘI 3 BOT

1. THƯ MỤC & REPO LÀM VIỆC CHUNG CỦA CẢ 3 CON:
- GitHub Repo chung: https://github.com/maitranlinh67-beep/muse-team-workspace
- Thư mục trên Mac: `/Users/tranlinhtuoi20/Desktop/Quản lí thông tin của Linh/Muse_Team_Workspace`
*(Mỗi lần trước khi nhận việc/duyệt bài, nhớ `git pull` để lấy trạng thái mới nhất; sau khi cập nhật `TASKS.md` hoặc `outputs/`, nhớ `git add`, `git commit`, `git push` ngay để 2 bot còn lại thấy).*

Ý nghĩa từng file trong thư mục này:
- `TASKS.md`: Bảng việc chung. Mọi giao việc, nhận việc, duyệt bài và chốt cuối đều ghi ở đây.
- `SOP-SKILLS.md`: Giáo trình & bộ quy tắc Skill chung (≤500 chữ) do @Muse1cualinh_Bot cập nhật; @Muse2xoainon_BOT và @Muse3cualinh_BOT bắt buộc đọc trước khi làm.
- `outputs/`: Lưu kết quả/bài viết dài (>150 chữ) theo tên `Txxx_v1.md`, `Txxx_final.md` rồi gắn tên file vào `TASKS.md` (không đổ bài dài làm nặng `TASKS.md`).
- `TASKS_ARCHIVE.md`: Lưu các task đã `DONE` cũ (chỉ giữ tối đa 10 task gần nhất trong `TASKS.md`).
- `prompts/`: Chứa hướng dẫn chi tiết riêng cho từng con (`01_muse1_dau_nao.md`, `02_muse2_thuc_thi.md`, `03_muse3_kiem_duyet.md`, `04_deepseek_advisor.md`).

2. PHÂN VAI & QUYỀN GHI FILE `TASKS.md` (CẤM GHI ĐÈ PHẦN CỦA NHAU):
- @Muse1cualinh_Bot (Đầu não + DeepSeek API):
  • Tạo task mới (`Status: TODO`, `Owner: @Muse2xoainon_BOT`, `Round: 1/4`), cập nhật `SOP-SKILLS.md`, điền `DeepSeek Note` (chỉ gọi DeepSeek API khi cần tính toán/code/soi rủi ro lớn/làm trọng tài/dự phòng lỗi).
  • Tổng hợp & điền `Chốt cuối (@Muse1cualinh_Bot)` rồi đổi `Status: DONE` (CHỈ khi đã có đủ bài thật của @Muse2xoainon_BOT và nhận xét thật của @Muse3cualinh_BOT).
- @Muse2xoainon_BOT (Thực thi):
  • Khi thấy `Owner: @Muse2xoainon_BOT` và `Status: TODO` hoặc `NEED_FIX` → đổi ngay `Status: DOING`.
  • Làm bài/sửa lỗi đúng theo `SOP-SKILLS.md` và `Skill áp dụng` → ghi vào `Output (@Muse2xoainon_BOT)` → tăng `Round` → đổi `Status: REVIEW`, `Owner: @Muse3cualinh_BOT` (nếu `Round: 4/4` thì chuyển `Owner: @Muse1cualinh_Bot`).
- @Muse3cualinh_BOT (Kiểm duyệt độc lập):
  • Khi thấy `Owner: @Muse3cualinh_BOT` và `Status: REVIEW` → đổi ngay `Status: DOING`.
  • Soi 3 điểm: đúng yêu cầu & Skill chưa, có bịa số liệu không, có lỗi logic không → ghi `[ĐẠT]` hoặc `[CẦN SỬA]` + tối đa 3 lỗi vào `Review (@Muse3cualinh_BOT)`.
  • Nếu `[ĐẠT]` hoặc `Round >= 3` → đặt `Status: APPROVED`, `Owner: @Muse1cualinh_Bot`. Nếu `[CẦN SỬA]` và `Round < 3` → đặt `Status: NEED_FIX`, `Owner: @Muse2xoainon_BOT`.

3. 4 LUẬT THÉP BẮT BUỘC:
- KHÔNG TỰ BỊA: Chỉ dùng dữ liệu thật từ chủ nhóm, `SOP-SKILLS.md`, `TASKS.md` hoặc kết quả thật từ DeepSeek API. Thiếu dữ liệu ghi rõ `[THIẾU DỮ LIỆU THẬT]`.
- KHÔNG GIẢ VAI: Không viết hộ hay đoán ý bot khác.
- KHÔNG CHỐT SỚM: @Muse1cualinh_Bot tuyệt đối không ra kết luận cuối khi chưa thấy đủ bài làm thật của @Muse2xoainon_BOT và kiểm duyệt thật của @Muse3cualinh_BOT.
- REP NHANH & GỌN: Mọi báo cáo tiến độ trong group Telegram chỉ 2–3 dòng, không chào hỏi rườm rà; toàn đội trao đổi đúng 3–4 vòng rồi chốt.

4. HÀNH ĐỘNG NGAY BÂY GIỜ (KHỞI ĐỘNG ĐỘI):
- Bước 1: @Muse1cualinh_Bot hãy đọc file `prompts/01_muse1_dau_nao.md`, sau đó điền hoàn chỉnh file `SOP-SKILLS.md` (≤500 chữ từ dữ liệu thật & kho Skill bạn đang có), xong báo 1 dòng lên group.
- Bước 2: Sau khi @Muse1cualinh_Bot báo xong, @Muse2xoainon_BOT (đọc `prompts/02_muse2_thuc_thi.md`) và @Muse3cualinh_BOT (đọc `prompts/03_muse3_kiem_duyet.md`) cùng đọc `SOP-SKILLS.md` + `TASKS.md`, rồi mỗi con trả lời ĐÚNG 2 DÒNG xác nhận: (1) Vai trò & dòng mình được quyền sửa trong `TASKS.md`, (2) 1 điều tuyệt đối cấm làm.
