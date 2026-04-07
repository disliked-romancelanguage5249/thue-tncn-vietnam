# Changelog - Thuế TNCN Vietnam Skill

> Ghi lại thay đổi quy định + cập nhật data skill. Dùng để kiểm tra Freshness.

## Format: [Ngày] - [Loại] - Mô tả

---

### 07/04/2026 - SKILL UPDATE - v1.7.0 (9+ Score Push)
- **CẢI THIỆN:** Rút gọn Rule 6-7-8 cho concise hơn (đổi cột "Hậu quả" thành "Fallback")
- **THÊM:** Calculation Checklist 8 bước - bắt buộc chạy trước khi output phép tính
- **THÊM:** Case 6: Expat cư trú + freelance (test Multi-Income routing)
- **THÊM:** Case 7: Chuyển đổi cư trú giữa năm (edge case)
- **CẬP NHẬT:** `sources.md` - NĐ hướng dẫn "đang dự thảo" (xác nhận qua search 07/04), thêm NQ 198 + NĐ 293
- **CẬP NHẬT:** Disclaimer timestamp 07/04/2026

### 07/04/2026 - SKILL UPDATE - v1.6.0 (Expat Tax Bracket Fix + Audit Sync)
- **FIX NGHIÊM TRỌNG:** Biểu thuế cư trú trong `nguoi-nuoc-ngoai-guide.md` sai (vẫn dùng 7 bậc cũ 2025)
  - Cũ: Bậc 3: 30-50tr (20%), Bậc 4: 50-80tr (25%), Bậc 5: >80tr (35%)
  - Mới: Bậc 3: 30-60tr (20%), Bậc 4: 60-100tr (30%), Bậc 5: >100tr (35%)
- **FIX:** Case 1 Expat tính lại - tách riêng BHTN (giống fix v1.4.0 cho Case 2)
  - Cũ: BHBB = 46,8tr x 10,5% = 4.914.000 (sai)
  - Mới: BHXH+BHYT trên trần 46,8tr + BHTN trên lương 80tr = 5.246.000
- **SỬA:** `system-flow.md` - cập nhật Mermaid diagram (5 rules -> 8 rules, thêm Multi-Income Check)
- **SỬA:** `faq.md` Q12 - phân biệt rõ biểu lũy tiến (lương) vs thuế suất % (CNKD)
- **THÊM:** changelog entry cho v1.5.0 (bổ sung retroactive)

### 07/04/2026 - SKILL UPDATE - v1.5.0 (Post-Audit Patch)
- **THÊM:** Multi-Income Check vào workflow (trước bước Load reference)
- **THÊM:** 3 Anti-Hallucination Rules mới (Rule 6, 7, 8):
  - Rule 6: Cấm tính nhẩm/gộp thuế lũy tiến - phải tách từng bước
  - Rule 7: User nhiều nguồn thu nhập -> bắt buộc load đồng thời nhiều file
  - Rule 8: Người làm công 1 nơi -> phải hỏi ủy quyền trước khi đưa SOP
- **SỬA:** Nhóm Đối Tượng "Người làm công ăn lương" - ghi rõ hỏi ủy quyền
- **SỬA:** Gate 2 Cross-Verify - thêm kiểm tra "Phép tính đúng từng bước?"

### 31/03/2026 - SKILL UPDATE - v1.4.0 (BHTN Trần Đóng Fix)
- **FIX LỖI QUAN TRỌNG:** Trần đóng BHTN ≠ trần đóng BHXH/BHYT
  - BHXH/BHYT: trần = 20 x lương cơ sở = 46.800.000 (NĐ 73/2024/NĐ-CP)
  - BHTN: trần = 20 x lương tối thiểu vùng (NĐ 293/2025/NĐ-CP + Luật Việc làm 2025)
- **THÊM:** Section "Trần Đóng Bảo Hiểm Bắt Buộc (2026)" vào `tong-quan-thue.md`
  - Bảng lương tối thiểu vùng I-IV theo NĐ 293/2025/NĐ-CP (hiệu lực 01/01/2026)
  - Bảng trần BHTN theo vùng: Vùng I (106,2tr), II (94,6tr), III (82,8tr), IV (74tr)
  - Tỷ lệ đóng NLĐ + NSDLĐ chi tiết
- **SỬA:** Case 2 trong `vi-du-tinh-thue.md` - tách riêng BHXH/BHYT/BHTN
  - Cũ: BHBB = 46.800.000 x 10,5% = 4.914.000 (sai)
  - Mới: BHXH+BHYT trên trần 46,8tr + BHTN trên lương thực tế = 4.946.000
- **SỬA:** Case 1 - ghi rõ lương 25tr chưa vượt trần nào, tính đúng 10,5%
- **THÊM:** NĐ 293/2025/NĐ-CP vào danh sách quy định theo dõi

### 25/03/2026 - SKILL UPDATE - v1.3.0 (Foreigner Tax Guide)
- **THÊM:** `nguoi-nuoc-ngoai-guide.md` - thuế TNCN cho người nước ngoài
- **NỘI DUNG:** Quy tắc cư trú 183 ngày, flat 20% (KCT), lũy tiến (CT)
- **NỘI DUNG:** DTA (Hiệp định tránh đánh thuế kép) với 80+ quốc gia
- **NỘI DUNG:** So sánh breakeven point cư trú vs không cư trú
- **NỘI DUNG:** Thủ tục xác nhận hoàn thành nghĩa vụ thuế khi xuất cảnh
- Thêm trigger keywords: expat, foreigner, non-resident, 183 ngày, DTA...

### 25/03/2026 - SKILL UPDATE - v1.2.0 (Thuế Khoán Expansion)
- **THÊm:** `thue-khoan-guide.md` - hướng dẫn chi tiết thuế khoán
- **CẬP NHẬT:** Thuế khoán bãi bỏ từ 01/01/2026 (NQ 198/2025/QH15)
- **CẬP NHẬT:** Ngưỡng miễn thuế HKD/CNKD tăng lên 500 tr/năm
- **CẬP NHẬT:** Lệ phí môn bài bãi bỏ (Luật 109/2025, Đ.35)
- **CẬP NHẬT:** Phân nhóm 4 tier mới (500tr/3tỷ/50tỷ)
- Thêm trigger keywords: thuế khoán, hộ kinh doanh, 01/CNKD...
- Cập nhật Số Liệu Nhanh và Quick Navigation trong SKILL.md

### 25/03/2026 - SKILL UPDATE - v1.1.0 (Audit Fix)
- Fix ngưỡng doanh thu: phân biệt rõ 3 mức (100tr TNCN, 200tr GTGT, 500tr kê khai)
- Fix decision tree trong freelancer-guide.md
- Fix Q12 thuế suất (bỏ số 15-20% sai)
- Thêm Verification Gate 3 bước vào workflow
- Thêm vi-du-tinh-thue.md (5 case studies)
- Thêm anti-hallucination rules
- Thêm Confidence Level cho mỗi reference file

### 25/03/2026 - SKILL CREATE - v1.0.0
- Tạo skill ban đầu với 6 reference files
- Nguồn: 7 web searches từ gdt.gov.vn, chinhphu.vn, tuoitre.vn, misa.vn...

---

## Quy Định Đã Theo Dõi

### 2026 - Thay đổi lớn
| Ngày hiệu lực | Văn bản | Nội dung |
|---------------|---------|---------|
| 01/01/2026 | NQ 198/2025/QH15 | **Bãi bỏ thuế khoán**, HKD chuyển kê khai tự nộp |
| 01/01/2026 | NQ 198/2025/QH15 | Ngưỡng miễn thuế HKD nâng lên **500 tr/năm** |
| 01/01/2026 | NQ 110/2025/UBTVQH15 | Giảm trừ gia cảnh tăng 40% (15,5tr + 6,2tr) |
| 01/01/2026 | Luật 109/2025/QH15 (áp dụng sớm) | Biểu thuế 5 bậc cho thu nhập lương |
| 01/01/2026 | Luật 109/2025/QH15, Đ.35 | Bãi bỏ lệ phí môn bài |
| 01/07/2025 | Luật 109/2025/QH15 | Sàn TMĐT khấu trừ thuế thay |
| 01/07/2025 | NĐ hướng dẫn | Ngưỡng GTGT nâng từ 100tr lên 200tr |
| 01/01/2026 | NĐ 293/2025/NĐ-CP | Lương tối thiểu vùng mới (I: 5,31tr, II: 4,73tr, III: 4,14tr, IV: 3,7tr) |
| 01/01/2026 | NĐ 293/2025 + Luật Việc làm 2025 | Trần BHTN = 20 x lương tối thiểu vùng (khác trần BHXH) |
| 01/07/2026 | Luật 109/2025/QH15 | Hiệu lực chính thức toàn bộ luật |

### Theo dõi tiếp (chưa có hiệu lực)
- NĐ hướng dẫn chi tiết Luật 109/2025 - chờ ban hành
- Thông tư hướng dẫn mẫu biểu mới (có thể thay thế TT 80/2021)

---

## Expiry Dates

| Reference file | Hết hạn | Lý do |
|---------------|---------|-------|
| deadline-tracker.md | 31/01/2027 | Lịch deadline hết kỳ 2026 |
| tong-quan-thue.md | 30/06/2027 | Kiểm tra luật mới mỗi năm |
| sop-quyet-toan.md | 30/04/2027 | SOP cho kỳ QT 2025-2026 |
| freelancer-guide.md | 30/06/2027 | Có thể thay đổi ngưỡng |
| thue-khoan-guide.md | 30/06/2027 | Theo dõi NĐ hướng dẫn chi tiết |
| faq.md | 30/06/2027 | Cần cập nhật theo quy định mới |
| vi-du-tinh-thue.md | 30/06/2027 | Cần cập nhật số liệu mới |
| nguoi-nuoc-ngoai-guide.md | 30/06/2027 | Theo dõi DTA mới + NĐ hướng dẫn expat |
