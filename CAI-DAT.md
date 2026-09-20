# Cài Nhuận sắc

Bạn chỉ cần file `SKILL.md` (hoặc `nhuansac-compact.zip`). Chọn đúng một cách hợp với công cụ bạn đang dùng.

| Bạn dùng | Cách nhanh nhất |
|---|---|
| Claude (claude.ai, app Claude) | Tải zip lên mục Skills, hoặc dán vào Project |
| ChatGPT | Dán vào Project hoặc Custom GPT |
| Claude Code | Chép thư mục vào `~/.claude/skills/` |
| Gemini hoặc công cụ khác có ô "hướng dẫn riêng" | Dán nội dung `SKILL.md` vào ô đó |

## Claude

**Cách 1: Skills (khuyên dùng)**

1. Mở claude.ai, vào **Settings** (Cài đặt), tìm mục **Skills** (có thể nằm trong **Capabilities**).
2. Chọn **Upload skill**, chọn file `nhuansac-compact.zip`.
3. Xong. Từ giờ trong mọi cuộc chat, bạn dán bài và nói "nhuận sắc" là skill tự chạy.

**Cách 2: Project**

1. Vào **Projects**, tạo Project mới tên "Nhuận sắc".
2. Mở phần **Instructions** (Hướng dẫn) của Project.
3. Mở `SKILL.md`, chép toàn bộ phần **bên dưới** dòng `---` thứ hai, dán vào ô Instructions, lưu lại.
4. Mỗi lần cần sửa bài, mở chat trong Project này.

## ChatGPT

**Cách 1: Project**

1. Vào **Projects**, tạo Project mới tên "Nhuận sắc".
2. Mở phần **Instructions** của Project.
3. Chép phần bên dưới dòng `---` thứ hai trong `SKILL.md` (khoảng 5.100 ký tự, dưới giới hạn 8.000), dán vào, lưu lại.

**Cách 2: Custom GPT** (hợp khi muốn gửi link cho người khác dùng)

1. Vào **GPTs**, chọn **Create**, chuyển sang tab **Configure**.
2. Name: `Nhuận sắc`. Description: `Gỡ giọng AI khỏi bài viết tiếng Việt và tiếng Anh, giữ nguyên nội dung`.
3. Instructions: dán phần bên dưới dòng `---` thứ hai trong `SKILL.md`.
4. Conversation starters gợi ý: `Nhuận sắc post Facebook này:`, `Chỉ rà bài này, đừng sửa:`.
5. Lưu, chọn chế độ chia sẻ "Only me" hoặc "Anyone with the link".

**Cách 3: Skills** (nếu tài khoản của bạn có mục này, thường ở gói Business, Enterprise, Edu): tải `nhuansac-compact.zip` lên như với Claude.

## Claude Code

```bash
mkdir -p ~/.claude/skills
cp -R nhuansac-compact ~/.claude/skills/nhuansac
```

Mở phiên Claude Code mới rồi gõ `/nhuansac`, hoặc dán bài và nói "nhuận sắc bài này".

## Kiểm tra đã cài đúng chưa

Dán đoạn này vào:

```
Nhuận sắc: Trong thời đại số hiện nay, việc chăm sóc khách hàng đóng một vai trò vô cùng quan trọng. Hãy cùng tìm hiểu 3 bí quyết dưới đây! Hy vọng bài viết hữu ích với bạn.
```

Cài đúng thì bạn nhận lại ba phần **Bản sửa**, **Đã sửa**, **Cần bạn kiểm tra**. Mở bài "Trong thời đại số" và câu "Hy vọng bài viết hữu ích" phải biến mất, và AI sẽ hỏi 3 bí quyết đó là gì thay vì tự nghĩ ra.

Nhận lại một bài viết lại bình thường, không có ba phần trên, thì nói rõ hơn: `Dùng skill Nhuận sắc để sửa đoạn này: …`

## Lưu ý

- Chỉ cài **một** bản: bản gọn này hoặc bản đầy đủ `nhuansac`. Cài cả hai thì chúng tranh nhau chạy.
- Dán hướng dẫn vào ô "Customize ChatGPT" (hướng dẫn chung cho mọi cuộc chat) thì không nên: ô đó ngắn hơn file này, và mọi cuộc chat của bạn sẽ bị ảnh hưởng.
