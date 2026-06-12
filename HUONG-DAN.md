# 📦 Hướng dẫn đưa profile README mới lên GitHub

Bộ này gồm:

```
ThanhhDuongg/
├── README.md                        ← README chính (đã trỏ tới các file SVG bên dưới)
├── assets/
│   ├── hero.svg                     ← Banner động: aurora + hiện tên từng chữ + hạt bay
│   ├── pipeline.svg                 ← Pipeline động: CODE → TEST → REVIEW → SHIP
│   └── skills.svg                   ← Equalizer kỹ năng nhấp nhô theo nhịp
└── .github/workflows/snake.yml      ← Tự động tạo "rắn ăn contribution" mỗi ngày
```

## Cách 1 — Cập nhật repo `ThanhhDuongg` hiện có (khuyên dùng)

Repo profile của bạn đã tồn tại, chỉ cần thay nội dung:

```bash
git clone https://github.com/ThanhhDuongg/ThanhhDuongg.git
cd ThanhhDuongg

# Xoá nội dung cũ (giữ .git), rồi copy toàn bộ file mới vào thư mục này
# (README.md, assets/, .github/)

git add -A
git commit -m "Redesign profile README with custom SVG animations"
git push origin main
```

## Cách 2 — Tạo repo mới hoàn toàn

> Lưu ý: GitHub chỉ hiển thị README trên trang cá nhân khi **tên repo trùng đúng username** (`ThanhhDuongg`). Nếu tạo repo mới, bạn cần xoá/đổi tên repo cũ trước.

1. Vào https://github.com/new → đặt tên repo là `ThanhhDuongg` → Public → Create.
2. Trong thư mục chứa các file này:

```bash
git init
git add -A
git commit -m "Initial profile README"
git branch -M main
git remote add origin https://github.com/ThanhhDuongg/ThanhhDuongg.git
git push -u origin main
```

## Kích hoạt animation con rắn 🐍

1. Sau khi push, vào tab **Actions** của repo → chọn workflow **Generate contribution snake** → bấm **Run workflow**.
2. Vào **Settings → Actions → General → Workflow permissions** → chọn **Read and write permissions** → Save (cần để workflow push được nhánh `output`).
3. Chạy xong, ảnh rắn sẽ tự hiện trong README (lúc đầu chưa chạy thì ô đó tạm trống — bình thường).

## Việc cần chỉnh tay (2 chỗ)

Trong `README.md`, phần **Connect With Me**:

- Thay `your-email@st.phenikaa-uni.edu.vn` bằng email thật của bạn.
- Thay `https://www.facebook.com/your-profile` bằng link Facebook/LinkedIn của bạn (hoặc xoá nút nếu không muốn).

## Vì sao bản này tốt hơn bản cũ?

- ✨ **3 animation SVG tự thiết kế riêng** (hero aurora, pipeline test, skill equalizer) — không phải template ai cũng có; hoạt động trực tiếp trên GitHub nhờ SMIL/CSS animation nhúng trong SVG.
- 🐛 **Sửa lỗi streak stats**: bản cũ dùng `herokuapp.com` đã ngừng hoạt động → đổi sang `streak-stats.demolab.com`.
- 🎯 **Định vị đúng hơn**: nhấn mạnh Software Engineering, Java/OOP, Testing/QA (đúng với các repo OOP.KTX, PTPM, SAD) thay vì chỉ data.
- 🎨 **Bảng màu thống nhất** xuyên suốt mọi widget: tím `#8B5CF6` · cyan `#22D3EE` · hồng `#F472B6` trên nền `#0B1020`.
- 🌗 Snake có cả bản dark/light tự đổi theo theme người xem.
