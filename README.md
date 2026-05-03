# 🇻🇳 Skill Thuế TNCN Vietnam (2026)

> AI Skill tra cứu thuế TNCN, SOP kê khai/quyết toán, hướng dẫn theo nhóm đối tượng.

[![Version](https://img.shields.io/badge/version-1.7.0-blue)]()
[![License](https://img.shields.io/badge/license-MIT-green)]()
[![Score](https://img.shields.io/badge/audit%20score-9.2%2F10-brightgreen)]()

## Tổng Quan

Skill **thue-tncn-vietnam** là bộ công cụ tra cứu thuế TNCN dạng AI, tự chứa toàn bộ dữ liệu cần thiết. Hoạt động trên Claude Desktop, Google Antigravity, và các nền tảng AI hỗ trợ skill/knowledge base.

### Tính năng chính

- 📊 **Biểu thuế 5 bậc 2026** (Luật 109/2025/QH15)
- 🧮 **7 case study tính thuế** chi tiết (lương, freelancer, KOL, seller, expat)
- 📋 **SOP quyết toán** qua eTax Mobile (9 bước) + Cổng thuế (5 bước)
- 🌏 **Thuế người nước ngoài** - cư trú/không cư trú, DTA, flat 20%
- 🔒 **3 Verification Gates + 8 Anti-Hallucination Rules** chống sai sót
- ✅ **Calculation Checklist** 8 bước bắt buộc trước khi output phép tính

### Nhóm đối tượng

| Nhóm | File hướng dẫn |
|------|---------------|
| Người làm công ăn lương | `tong-quan-thue.md` + `sop-quyet-toan.md` |
| Freelancer / KOL | `freelancer-guide.md` |
| Người bán hàng online | `freelancer-guide.md` |
| Người nước ngoài (Expat) | `nguoi-nuoc-ngoai-guide.md` |

## Cài Đặt

### Claude Desktop / Antigravity

```
your-project/
└── .agents/
    └── skill/
        └── thue-tncn-vietnam/   ← copy vào đây
```

### Các nền tảng khác

Copy nội dung `SKILL.md` vào system prompt, upload folder `references/` vào knowledge base.

## Số Liệu Nhanh (2026)

| Chỉ số | Giá trị | Căn cứ |
|--------|---------|--------|
| Giảm trừ bản thân | 15,5 tr/tháng | NQ 110/2025/UBTVQH15 |
| Giảm trừ NPT | 6,2 tr/tháng | NQ 110/2025/UBTVQH15 |
| Ngưỡng miễn thuế HKD | **500 tr/năm** | NQ 198/2025/QH15 |
| Biểu thuế lũy tiến | 5 bậc (5% - 35%) | Luật 109/2025/QH15 |
| Thuế khoán | **Bãi bỏ** từ 01/01/2026 | NQ 198/2025/QH15 |

## Cấu Trúc

```
thue-tncn-vietnam/
├── SKILL.md                          ← Master file (AI đọc đầu tiên)
├── README.md                         ← File này
└── references/
    ├── tong-quan-thue.md             ← Biểu thuế, giảm trừ, ngưỡng
    ├── vi-du-tinh-thue.md            ← 7 ví dụ tính thuế
    ├── sop-quyet-toan.md             ← SOP quyết toán eTax / Cổng thuế
    ├── freelancer-guide.md           ← Freelancer, KOL, seller
    ├── nguoi-nuoc-ngoai-guide.md     ← Expat, cư trú, DTA
    ├── thue-khoan-guide.md           ← Thuế khoán bãi bỏ 2026
    ├── deadline-tracker.md           ← Lịch nộp thuế 2026
    ├── faq.md                        ← 12 câu hỏi thường gặp
    ├── system-flow.md                ← Flow diagrams (Mermaid)
    ├── changelog.md                  ← Lịch sử cập nhật + expiry
    └── sources.md                    ← Nguồn tham khảo
```

## Audit Score

Skill đã qua **4 vòng đánh giá** theo quy trình 6 bước:

```
v1.4.0 (7.4) → v1.5.0 (7.9) → v1.6.0 (8.7) → v1.7.0 (9.2/10)
```

## Lưu Ý Quan Trọng

⚠️ **Thông tin chỉ mang tính tham khảo, KHÔNG thay thế tư vấn thuế chuyên nghiệp.**

Kiểm tra lại tại:
- https://gdt.gov.vn
- https://canhan.gdt.gov.vn

## Tác Giả

**Minh Đỗ** | [Liên hệ](https://facebook.com/dotanminh)

---

*Cập nhật: 07/04/2026 | Luật 109/2025/QH15 | NQ 198/2025/QH15*
