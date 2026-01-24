# 🧧 Lì Xì May Mắn - IT Department

Website Lì Xì May Mắn cho phòng IT! Người dùng click vào bao lì xì để nhận ngẫu nhiên số tiền và lời chúc may mắn.

![Preview](preview.png)

## ✨ Tính năng

- 🎁 Bao lì xì với animation mở đẹp mắt
- 💰 Số tiền ngẫu nhiên (10k - 500k VNĐ)
- 🎊 Lời chúc may mắn dành cho dân IT
- 🎉 Hiệu ứng confetti khi mở
- 📱 Responsive trên mobile
- 📤 Chia sẻ kết quả

## 🚀 Cách deploy lên GitHub Pages

### Bước 1: Tạo Repository mới

1. Đăng nhập GitHub
2. Click **"New repository"**
3. Đặt tên: `lucky-money` (hoặc tên khác)
4. Chọn **Public**
5. Click **"Create repository"**

### Bước 2: Upload files

**Cách 1: Upload trực tiếp trên GitHub**

1. Trong repository mới, click **"uploading an existing file"**
2. Kéo thả file `index.html` vào
3. Click **"Commit changes"**

**Cách 2: Dùng Git command line**

```bash
# Clone repository
git clone https://github.com/YOUR_USERNAME/lucky-money.git
cd lucky-money

# Copy file index.html vào folder
# Sau đó commit và push
git add .
git commit -m "Initial commit"
git push origin main
```

### Bước 3: Bật GitHub Pages

1. Vào **Settings** của repository
2. Scroll xuống **Pages** (menu bên trái)
3. Trong **Source**, chọn:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click **Save**
5. Đợi 1-2 phút để deploy

### Bước 4: Truy cập website

Website sẽ có địa chỉ:
```
https://YOUR_USERNAME.github.io/lucky-money/
```

## 🖼️ Thêm hình ảnh tiền thật (Tùy chọn)

Nếu muốn thêm hình ảnh tiền Việt Nam thật:

1. Tạo folder `images/` trong repository
2. Thêm các file ảnh tiền:
   - `10000.png`
   - `20000.png`
   - `50000.png`
   - `100000.png`
   - `200000.png`
   - `500000.png`

3. Sửa code trong `index.html`, tìm đoạn sau và uncomment:

```javascript
// Thay đổi phần moneyImageEl.innerHTML trong function openEnvelope()
moneyImageEl.innerHTML = `
    <img src="images/${currentResult.money.image}.png" 
         alt="${currentResult.money.display} VNĐ">
`;
```

## ⚙️ Tùy chỉnh

### Thay đổi số tiền

Sửa mảng `moneyAmounts` trong file `index.html`:

```javascript
const moneyAmounts = [
    { value: 10000, display: '10.000', image: '10000' },
    { value: 20000, display: '20.000', image: '20000' },
    // Thêm hoặc sửa các giá trị khác
];
```

### Thay đổi lời chúc

Sửa mảng `wishes` trong file `index.html`:

```javascript
const wishes = [
    "Chúc bạn năm mới code không bug! 🚀",
    "Thêm lời chúc mới ở đây...",
    // ...
];
```

### Thay đổi màu sắc

Sửa CSS variables ở đầu file:

```css
:root {
    --red-primary: #C41E3A;
    --red-dark: #8B0000;
    --gold-primary: #FFD700;
    /* ... */
}
```

## 📝 License

Free to use for IT Department! 🎉

---

Made with ❤️ for Tết 2025
# luckymoney
