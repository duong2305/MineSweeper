# Dò mìn (Minesweeper)

Game web tĩnh viết bằng HTML, CSS và JavaScript thuần. High score được lưu bằng `localStorage` của trình duyệt, nên không cần database hoặc backend.

## Chạy trên máy

Mở `index.html` bằng trình duyệt, hoặc dùng extension **Live Server** trong VS Code.

## Deploy public bằng GitHub Pages

1. Trên GitHub, tạo repository **public**, ví dụ: `minesweeper`.
2. Mở PowerShell tại thư mục dự án, sau đó chạy lệnh dưới đây. Thay `YOUR-USERNAME` bằng username GitHub của bạn:

```powershell
git init
git add index.html README.md .github/workflows/deploy.yml
git commit -m "Create Minesweeper game"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/minesweeper.git
git push -u origin main
```

3. Vào repository GitHub: **Settings** → **Pages** → mục **Build and deployment / Source**, chọn **GitHub Actions**.
4. Vào tab **Actions** để xem workflow `Deploy Minesweeper to GitHub Pages`. Khi workflow thành công, game có URL:

```text
https://YOUR-USERNAME.github.io/minesweeper/
```

Mỗi lần `git push` lên nhánh `main` sau đó sẽ tự deploy lại trang.

## High score

- Lưu tối đa 5 thành tích cho mỗi mức Dễ, Vừa, Khó.
- Dữ liệu chỉ nằm trên trình duyệt/thiết bị đang chơi.
- Nếu xóa dữ liệu website, đổi trình duyệt hoặc đổi thiết bị, bảng điểm sẽ không đi theo.
- Muốn làm leaderboard chung cho nhiều người chơi cần bổ sung database/backend, ví dụ Supabase hoặc Firebase.