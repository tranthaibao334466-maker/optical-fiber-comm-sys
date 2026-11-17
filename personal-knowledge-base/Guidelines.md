---
aliases:
  - Quy tắc viết note, Note template, Hướng dẫn viết ghi chú
tags:
- meta
- vault
- guideline
status: verified
sources: vault CLAUDE.md ( personal-knowledge-base)
updated: 2026-11-10
---

# Note Writing Guidelines

**Quy tắc hình thức khi viết ghi chú từ sách giáo trình vào vault, để Claude đọc và kiểm chứng được.**

## 1. Tên file và phạm vi

- Một khái niệm một ghi chú.
- Tên file là tên khái niệm bằng tiếng Anh, ví dụ `Group Velocity Dispersion.md`.
- Nếu một ghi chú bắt đầu bàn hai khái niệm, tách ra và nối bằng liên kết.

## 2. Frontmatter (đầu ghi chú)

markdown

```markdown
---
aliases: [GVD, tán sắc vận tốc nhóm]
tags: [fiber, dispersion]
status: draft          # verified | draft | unverified
sources: ["Keiser, Ch. 3, p. 85"]
updated: YYYY-MM-DD
---
```

- `aliases`: tên gọi khác, kể cả tiếng Việt, để tìm kiếm không bị sót.
- `status`:
    - `draft`: mới viết từ sách, chưa đối chiếu.
    - `verified`: chỉ đặt sau khi đọc lại đoạn được trích và xác nhận khớp.
    - `unverified`: từ trí nhớ, bài giảng hoặc web. Coi là gợi ý, không phải sự thật.
- `sources`: sách, chương, trang. Đây là phần quan trọng nhất. Chưa nhớ trang thì ghi chương và giữ `draft`. Không đoán số trang.

## 3. Nội dung bên trong

- **Một dòng tóm tắt** ngay dưới tiêu đề, để Claude biết có cần đọc tiếp không.
- **Intuition**: một ví dụ đời thường ngắn. Đây cũng là cách tự kiểm tra mình đã hiểu chưa.
- **Công thức** viết bằng LaTeX: `$...$` trong dòng, `$$...$$` cho công thức riêng. Với mọi ký hiệu, ghi rõ ý nghĩa và đơn vị ngay bên dưới.
- Ký hiệu khác nhau giữa các sách (ví dụ dấu của số hạng tán sắc trong NLSE), nên ghi rõ đang theo sách nào.
- **Viết bằng lời của mình**, không chép nguyên văn. Chỉ trích đoạn ngắn khi thật cần.
- Mục **Ghi chú cá nhân** riêng cho ý kiến của bạn, không trộn với nội dung sách.

## 4. Liên kết

- Dùng `[[Tên Ghi Chú]]` cho các khái niệm liên quan.
- Liên kết tới ghi chú chưa tồn tại là chấp nhận được. Nó cho biết mục cần viết thêm.
- Mục **Open questions** ghi chỗ chưa hiểu hoặc chưa chắc.

## 5. Hình ảnh

Claude đọc text tốt hơn hình. Khi chụp hình từ sách, kèm một dòng mô tả bằng chữ: hình thể hiện gì, trục nào, kết luận gì. Hình không có mô tả gần như vô hình với Claude.

## 6. Nên tránh

- Gộp nhiều khái niệm vào một ghi chú dài.
- Đặt `verified` khi chưa đối chiếu.
- Trộn ý kiến cá nhân với nội dung sách mà không đánh dấu.
- Ghi nguồn không có thật hoặc số trang đoán.

## Mẫu ghi chú

markdown

```markdown
---
aliases: []
tags: []
status: draft
sources: []
updated: YYYY-MM-DD
---

# Concept name

**Tóm tắt một dòng.**

## Intuition
Ví dụ đời thường ngắn.

## Definition and equations
Ký hiệu, đơn vị, giả định, giới hạn áp dụng.

## Ghi chú cá nhân
- ...

## Links
Related: [[...]]

## Open questions
- ...
```